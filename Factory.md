# 工廠

* ## Factory
定義一個創建對象的接口，讓其子類自己決定實例化哪一個工廠類，工廠模式使其創建過程延遲到子類進行。

```
function Developer(name){
    this.name = name;
    this.type = 'Developer';
};

function Tester(name){
    this.name = name;
    this.type = 'Tester';
};

function EmployeeFactory(){
    this.creat = (name, type) => {
        switch(type){
            case 1:
                return new Developer(name); break;
            case 2:
                return new Tester(name); break;
        }
    };
};

const employeeFactory = new EmployeeFactory();
const employees = [];

employees.push(employeeFactory.creat("Patrick",1));
employees.push(employeeFactory.creat("John",2));
console.log(employees) 
// [ 
//     Developer { name: 'Patrick', type: 'Developer' },
//     Tester { name: 'John', type: 'Tester' }
// ]
```

另一種類別為基礎的創建型模式。
提供通用的介面委派物件實例化的職責至其子類別之中。

這個模式經常被使用在，我們需要同時管理與操作，多個有相似特性卻仍不同的物件集合。


