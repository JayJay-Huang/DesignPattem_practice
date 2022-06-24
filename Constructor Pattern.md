類別為基底的創建式設計模式。
建構子是一個特殊的function可以用來實例化新物件中所定義的方法與屬性。

### js 的建構子模式
建構子模式是Javascript裡，最普遍使用來創建給定新物件的一種設計模式。

```
// traditional Function-based syntax
function Hero(name, power){
    this.name = name;
    this.power = power;
    this.getDetails = function(){
        return this.name + '-' + this.power;
    };
};

// ES6 Class syntax
class Hero{
    constructor(name, power){
        this.name = name;
        this.power = power;
        this.getDetails = function(){
            return this.name + ' - ' + this.power;
        };
    };
};

const IronMan = new Hero('Iron Man', 'fly');
console.log(IronMan.getDetails()); // Iron Man - fly
```