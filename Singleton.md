# 單例 singleton

把初始化(建構子)隱藏起來。
對外提供一個靜態方法。


```
function Process(state){
    this.state = state;
};

const Singleton = (function(){
    function ProcessManager(){
        this.numProcess = 0;
    };

    let pManager;
    
    function creatProcessManager(){
        pManager = new ProcessManager();
        return pManager;
    };

    return {
        getProcessManager:() => {
            if(!pManager) pManager = creatProcessManager();
            return pManager;
        }
    };
})()

未完

```
// https://www.youtube.com/watch?v=JKNjfDCNPa4&ab_channel=DevSage

### eager initialization
飢餓模式初始化

### lazy initialization
懶惰模式初始化






