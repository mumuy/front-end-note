### 对象深度克隆
``` javascript
Object.prototype.clone = function () {
    var newObj = {};
    for (var i in this) {
        console.log("i = " + i)
        if (typeof(this[i]) == 'object'|| typeof(this[i]) == 'function') {
            newObj[i] = this[i].clone()
        } else {
            newObj[i] = this[i]
        }
    }
    return newObj
}
```

#### 简单的克隆：
方法一
``` javascript
obj = eval(uneval(o));
```
方法二(系列化对象)
``` javascript
obj= JSON.parse(JSON.stringify(o));
```

### 数组深度克隆
``` javascript
Array.prototype.clone = function () {
    var newArray = []
    for (var i = 0; i < this.length; i++) {
        if (typeof(this[i]) == 'object' || typeof(this[i]) == 'function') {
            newArray[i] = this[i].clone()
        } else {
            newArray[i] = this[i]
        }
    }
    return newArray
}
```

### 函数深度克隆
``` javascript
Function.prototype.clone = function () {
    var that = this;
    var newFunc = function () {
        return that.apply(this, arguments);
    };
    for (var o in this) {
        newFunc[o] = this[o];
    }
    return newFunc;
}
```