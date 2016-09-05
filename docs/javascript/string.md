### 字符串去重
```javascript
"aagbdfcedskahkxxbhxbshb".replace(/(\w)(?=\w*\1)/gi,"");
```


### 字符串反序列化成JSON
eval方式解析
```javascript
function strToJson(str){
	var json = eval_r('(' + str + ')');        //或eval('('+Json+')')
	return json;
}
```
new Function形式
```javascript
function strToJson(str){
	var json = (new Function("return " + str))();
	return json;
}
```
使用全局的JSON对象
```javascript
function strToJson(str){
	return JSON.parse(str);
}
```

### 补零
```javascript
function pad(s) {
  return ('0' + s).slice(-2);
}
```