### 数组复制技巧
方法一
``` javascript
var a = [1,2,3];
b = a.slice(0);
```
方法二
``` javascript
var a = [1,2,3];
b = a.concat();
```

### 打乱数字数组的顺序
``` javascript
numbers.sort(function(){ return Math.random() - 0.5});
```

### 给数组创建一个随机项
``` javascript
var items = [12, 548 , 'a' , 2 , 5478 , 'foo' , 8852, , 'Doe' , 2145 , 119];
var randomItem = items[Math.floor(Math.random() * items.length)];
```

### 数组追加
``` javascript
Array.prototype.push.apply(array1, array2);
```

### 获得数组中的最大值
写法一
``` javascript
var a = [10,1,2,3,4,8,9];
Math.max.apply(null,a);
```
写法二
``` javascript
Array.prototype.max = function() {
    return Math.max.apply({},this); 
}
```

### 类数组转换成数组
写法一
``` javascript
var args = Array.prototype.slice.call(arguments, 0);
```
写法二
``` javascript
var args = [].slice.call(arguments);
```
ES6的实现
``` javascript
var args = Array.from(arguments);
```

### 不用for循环创造0～100的数组
``` javascript
Array.from({length:100}).map(function(item,index){return index});
```
``` javascript
Array(100).join(",").split(",").map(function(key,index){return index;});
```
``` javascript
Object.keys(Array(100).toString().split(","));
```