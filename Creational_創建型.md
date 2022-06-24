
# Creational

在創建的同時，隱藏創建方法(邏輯)。
而不是使用新的運算符直接實例化對象。
使得需要創建哪些對象時更加靈活。


---

# Factory pattern

# Abstrat pattern

# Singleton patten
保證一類只有一例項。
先判斷例項存在否，有則返回，無則建立在返回。

1. 透過objext直接量建立
```
let mySingleton = {
    pro1: 'jay',
    pro2: '0920',
    method: ()=>{
        console.log("hello~");
    }
};
mySingleton.method() // hello~
console.log(mySingleton.pro1) // jay
console.log(mySingleton.pro2) // 0920
```
2. 私有屬性方法
```
let mySingleton = ()=>{

    let name = 'Jay';
    function sayName(){
        // console.log(`My name is ${name}`)
        return name;
    };
    return {
        sayHi: ()=>{
            console.log('hello~')
        },
        sayName: sayName()
    }
};
mySingleton(); // hello~
console.log(mySingleton().sayName = 'KKK'); // KKK
console.log(mySingleton().sayName); // Jay
```
3. 建構函式的寫法
```
function Construct(){
    // 確保只有單例
    if( Construct.unique !== undefined ){
    // 或 (typeof Construct.unique === 'object')
        return Construct.unique
    }
    this.name = "Jay";
    this.age = "24";
    Construct.unique = this
};
let a = new Construct();
let b = new Construct();
console.log(a===b); // true
console.log(a); // Construct { name: 'Jay', age: '24' }
console.log(b); // Construct { name: 'Jay', age: '24' }
```

# Builder patten

# Prototype patten

