横屏监听
``` javascript
var updateOrientation =function(){
    if(window.orientation=='-90'|| window.orientation=='90'){
        console.log('为了更好的体验，请将手机/平板竖过来！');
     }else{
        console.log('竖屏状态');
    }
};
window.onorientationchange= updateOrientation;
```
