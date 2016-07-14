### 横屏监听
``` javascript
var updateOrientation =function(){
    if(window.orientation=='-90'|| window.orientation=='90'){
        console.log('为了更好的体验，请将手机/平板竖过来！');
     }else{
        console.log('竖屏状态');
    }
};
var supportsOrientationChange = "onorientationchange" in window,
    orientationEvent = supportsOrientationChange ? "orientationchange" : "resize";// 监听事件
window.addEventListener(orientationEvent,updateOrientation);
```
