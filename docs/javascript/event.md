通用事件兼容框架：[EventUtil](https://github.com/mumuy/tools-library/blob/gh-pages/code/EventUtil.js)

### 取消浏览器默认行为
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

### 阻止事件冒泡
``` javascript
function stopBubble(e){
    if (e && e.stopPropagation) {
        e.stopPropagation();
    }else if (window.event) {
        window.event.cancelBubble = true;
    }
}
```

### 模拟触发点击事件
``` javascript
function simulateClick(el) {
  var evt;
  if (document.createEvent) { // DOM Level 2 standard
    evt = document.createEvent("MouseEvents");
    evt.initMouseEvent("click", true, true, window, 0, 0, 0, 0, 0, false, false, false, false, 0, null);
    el.dispatchEvent(evt);
  } else if (el.fireEvent) { // IE
    el.fireEvent('onclick');
  }
}
```

``` javascript
createEvent(eventType)
```
|参数|描述|
|-----|-----|
|eventType|想获取的 Event 对象的事件模块名。|

#### 返回值
返回新创建的 Event 对象，具有指定的类型。

#### 抛出
如果实现支持需要的事件类型，该方法将抛出代码为 NOT_SUPPORTED_ERR 的 DOMException 异常。

#### 说明
该方法将创建一种新的事件类型，该类型由参数 eventType 指定。注意，该参数的值不是要创建的事件接口的名称，而是定义那个接口的 DOM 模块的名称。

下表列出了 eventType 的合法值和每个值创建的事件接口：
eventType 的合法值和每个值创建的事件接口：

|参数|事件接口|初始化方法|
|-----|-----|-----|
|HTMLEvents|HTMLEvent|iniEvent()|
|MouseEvents|MouseEvent|iniMouseEvent()|
|UIEvents|UIEvent|iniUIEvent()|
用该方法创建了 Event 对象以后，必须用上表中所示的初始化方法初始化对象。
