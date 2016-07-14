### 是否存在某个class
``` javascript
function hasClass(node,classname){
  return node.className.match(new RegExp('(\\s|^)'+cls+'(\\s|$)'));
}
```

### 对节点增加class
``` javascript
function addClass(node,classname){
  if(!this.hasClass(node,classname)){
    node.className = (node.className+" "+classname).replace(/^\s+|\s+$/g,'');
  }
}
```

### 对节点删除class
``` javascript
function removeClass(node,classname){
  node.className = (node.className.replace(classname,"")).replace(/^\s+|\s+$/g,'');
}
```
