### 防抖（Debouncing/Debounce）

debounce 的关注点是空闲的间隔时间,强制函数在某段时间内只执行一次。

空闲控制 返回函数连续调用时，空闲时间必须大于或等于 delay，fn 才会执行

```javascript
function debounce(fn,delay){
	var timer;
	return function(){
		var context = this;
		var args = arguments;
		timer&&clearTimeout(timer);
		timer = setTimeout(function(){
			fn.apply(context,args);
		},delay);
	}
}
```


### 节流（Throttling/Throttle）

throttle 的关注点是连续的执行间隔时间,强制函数以固定的速率执行。

频率控制 返回函数连续调用时，action 执行频率限定为 次 / delay

```javascript
function throttle(fn, threshhold){
	var last;
	var timer;
	threshhold || (threshhold = 250);
	return function(){
		var context = this;
		var args = arguments;
		var now = + new Date();
		if(last && now < last + threshhold){
			timer&&clearTimeout(timer);
			timer = setTimeout(function(){
				last = now;
				fn.apply(context, args);
			},threshhold);
		}else{
			last = now;
			fn.apply(context,args);
		}
	}
}
```