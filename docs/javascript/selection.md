### 禁止用户选中文本
```javascript
var clearSlct= "getSelection" in window ? function(){
    window.getSelection().removeAllRanges();
} : function(){
    document.selection.empty();
};

//防止鼠标选中内容（当鼠标松开时清除选中内容）
window.onmouseup=function(){
    clearSlct();
}

//防止通过键盘选中内容（当按键松开时清除选中内容）
window.onkeyup=function(){
    clearSlct();
}
```