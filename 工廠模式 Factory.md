# Factory 工廠
當程式複雜度高的時候時候，可以利用此模式切割。

角色 : 
1.Factory: 切換介面角色
2.ConcreteProduct: 具體產生的產品實體。
3.Product: 抽象介面。

#### C#
```
    public static class BirdFactory
    {
        public static IBird GetBird(string birdName)
        {
            switch (birdName)
            {
                case "Swan":
                    return new Swan();

                case "Eagle":
                    return new Eagle();

                default:
                    throw new Exception("missing matching bird name");
            }
        }
    }
    public interface IBird
    {
        string Name { get; set; }
        void Fly();
    }
    public class Eagle : IBird
    {
        public string Name { get; set; } = "老鷹";
        public void Fly()
        {
            Console.WriteLine( Name + "飛飛飛飛");
        }
    }
    public class Swan : IBird
    {
        public string Name { get; set; } = "天鵝";
        public void Fly()
        {
            Console.WriteLine(Name + "游游游游");
        }
    }
```