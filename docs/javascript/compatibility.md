跨浏览器DOM对象：[DOMUtil](https://github.com/mumuy/tools-library/blob/gh-pages/code/DOMUtil.js)

### 获取指定class名称的DOM对象
``` javascript
function getElementsByClassNamefunction(className,context,tagName){
	if(typeof context == 'string'){
		tagName = context;
		context = document;
	}else{
		context = context || document;
		tagName = tagName || '*';
	}
    if(context.getElementsByClassName){
        return context.getElementsByClassName(className);
    }
    var nodes = context.getElementsByTagName(tagName);
    var results= [];
    for (var i = 0; i < nodes.length; i++) {
        var node = nodes[i];
        var classNames = node.className.split(' ');
        for (var j = 0; j < classNames.length; j++) {
            if (classNames[j] == className) {
                results.push(node);
                break;
            }
        }
    }
    return results;
}
```

### 获取选中文本内容
``` javascript
function getSelectedText() {
    if (window.getSelection) {
        return window.getSelection().toString();    
    }else if (document.getSelection) {
        return document.getSelection();
    }else if (document.selection) {
        return document.selection.createRange().text;
    }
}
```

### 跨浏览器获取可视窗口大小
``` javascript
function getWindow () {
    if(typeof window.innerWidth !='undefined') {
        return{
            width : window.innerWidth,
            height : window.innerHeight
        }
    }else{
        return {
            width : document.documentElement.clientWidth,
            height : document.documentElement.clientHeight
        }
    }
}
```
