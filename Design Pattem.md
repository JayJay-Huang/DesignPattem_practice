「Any problem in computer science can be solved by anther layer of indirection.」

# Creational pattem

* ## Factory
定義一個創建對象的接口，讓其子類自己決定實例化哪一個工廠類，工廠模式使其創建過程延遲到子類進行。

* ## Abstract Factory
提供一個創建一系列相關或相互依賴對象的接口，而無需指定它們具體的類。

* ## Singleton
保證一個類僅有一個實例，並提供一個訪問它的全局訪問點。
一個類，它在任何情況下都只會產生一個實例(多線程異常情況除外)。
為了取代使用全局變量的情況。
( 直接使用全局變量有很多局限性，比如可能會被實例化多次，不能靈活擴展成多個，難以支持延遲實例化(就是到真正使用時才實例化)等... )
![singleton_1](/mig/singleton_1.png)
中間層的思考：
單件模式在系統和全局變量之間中添加了一個中間層，之前系統直接調用全局變量，而使用單件模式後，系統使用類靜態方法Instance來獲取全局實例。在Instance函數中可以做很多事情，包括延遲實例以及指定實例數量，甚至返回不同的子類實例。

* ## Builder
將一個複雜的構建與其表示相分離，使得同樣的構建過程可以創建不同的表示。
* ## Prototype
用原型實例指定創建對象的種類，並且通過拷貝這些原型創建新的對象。

---

# Structural pattem
結構型模式涉及到如何組合類和對象以獲得更大的結構。

* ## Adapter適配器
適配器模式要解決的就是新加模塊與系統已有接口不匹配的問題。
![adapter_1](/mig/adapter_1.png)

* ## Bridge
* ## Filter、Criteria 
* ## Composit
* ## Decorator
* ## Facade
* ## Flyweight
* ## Proxy

---

# Behavioral pattem
行為模式涉及到算法和對象間職責的分配。行為模式不僅描述對象或類的模式，還描述它們之間的通信模式。

## Chain of Responsibility
## Command
## Interpreter



