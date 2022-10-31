# 單例 singleton

把初始化(建構子)隱藏起來。
對外提供一個靜態方法。

### eager initialization
飢餓模式初始化

### lazy initialization
懶惰模式初始化

----
目的：保證一個類別只會產生一個物件，而且要提供存取該物件的統一方法。

#### js
Singleton 意思是特定 class 只會有一個實例，當你第二次透過同個 class 建立實例時，亦只會得到同一個實例。
```
const instance1 = new Singleton();
const instance2 = new Singleton();
console.log(instance1 === instance2); //true
```
```
class Animal{
    constructor(){
        if(typeof Animal.cache === 'object') return Animal.cache;
        this.werght = 10;
        Animal.cache = this;
    }
}

let aaa = new Animal();
let bbb = new Animal();
console.log(aaa === bbb); //true

```
#### C#
```
public class Sun
{
    private string power = "陽光";
    
    private static Sun sun = null;
    private Sun(){
    }
    public static Sun getSun()
    {
        if(sun == null)
        {
            sun = new Sun();
        }
        return sun;
    }
    public void sunshine()
    {
        Console.WriteLine(this.power);
    }
}
```

### C++
