Zepto中的IIFE应用
```javascript
(function(global,factory){
    if(typeof define==='function'&& define.amd)
        define(function(){
            return factory(global)
        })
    else factory(global)
}(this,function(window){

}))
```