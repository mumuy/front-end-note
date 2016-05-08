通用事件兼容框架：[EventUtil](https://github.com/mumuy/tools-library/blob/gh-pages/code/EventUtil.js)

取消浏览器默认行为
``` javascript
function stopDefault( e ) {
    if ( e && e.preventDefault ){
        e.preventDefault();
    }else{
        window.event.returnValue = false;
    }
    return false;
}
```

阻止事件冒泡
``` javascript
function stopBubble(e){
    if (e && e.stopPropagation) {
        e.stopPropagation();
    }else if (window.event) {
        window.event.cancelBubble = true;
    }
}
```
