### 获取某月天数
```javascript
var day = new Date(2014,4,0);  //获取4月份的天数
var count = day.getDate();
```

### 日期对象转换成时间戳
```javascript
var d = +new Date(); 	//1466489912445
```

### yyyy-mm-dd 格式
传统浏览器
```javascript
var dt = new Date();
var date = [
  [dt.getFullYear(), dt.getMonth() + 1, dt.getDate()].join('-'),
  [dt.getHours(), dt.getMinutes(), dt.getSeconds()].join(':')
].join(' ').replace(/(?=\b\d\b)/g, '0'); // 正则补零 (略微改动)

console.log(date); // => 2016-03-25 11:01:01
```

现代浏览器
```javascript
var dt = new Date();
dt.setMinutes(dt.getMinutes() - dt.getTimezoneOffset()); // 修正时区偏移
var date = dt.toISOString().slice(0, -5).replace(/[T]/g, ' ');

console.log(date); // => 2016-03-25 11:01:01
```