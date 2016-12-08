### 经纬度
``` javascript
if(navigator.geolocation){
    navigator.geolocation.getCurrentPosition(function(position){
        console.log('纬度:'+position.coords.latitude,'经度：'+position.coords.longitude);
    });
}else{
    alert('不支持地理定位'); 
}
```
latitude        纬度

longitude       经度

accuracy        准确角

altitude        海拔高度

altitudeAcuracy     海拔高度的精确度

heading         行进方向

speed           地面的速度

安全限制：目前只有开启'https'协议才可以访问接口

被墙：Chrome的Geolocation如果你使用Fiddler抓包能看到浏览器在请求 "http://www.googleapis.com" 获得经纬度。而这个域名因为众所周知的原因会失败。
