### 添加cookie
``` javascript
function addCookie(objName,objValue,objHours,objDomain,objPath){
    var str = objName + "=" + escape(objValue);
    if(objHours > 0){ //为时不设定过期时间，浏览器关闭时cookie自动消失
        var date = new Date();
        var ms = objHours*3600*1000;
        date.setTime(date.getTime() + ms);
        str += "; expires=" + date.toGMTString();
        if(objDomain){
            str += ";domain="+objDomain;
        }
        if(objPath){
            str += ";path="+objPath;
        }
    }
    document.cookie = str;
}
```

### 获取指定名称的cookie的值
``` javascript
function getCookie(objName){
  var arrStr = document.cookie.split("; ");
  for(var i = 0;i < arrStr.length;i ++){
    var temp = arrStr[i].split("=");
    if(temp[0] == objName) return unescape(temp[1]);
  }
}
```

### 删除指定名称的cookie，可以将其过期时间设定为一个过去的时间
``` javascript
function delCookie(name){
  var date = new Date();
  date.setTime(date.getTime() - 10000);
  document.cookie = name + "=a; expires=" + date.toGMTString();
}
```
