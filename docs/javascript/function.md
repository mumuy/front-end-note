### 执行前判断
``` javascript
Function.prototype.before = function(fn) {
    var __self = this;
    return function() {
        if(fn.apply(this, arguments) === false) {
            return false;
        }
        return __self.apply(this, arguments);
    }
};
```