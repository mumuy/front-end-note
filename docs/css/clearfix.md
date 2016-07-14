### 常用的清除浮动方法:
方案一
``` CSS
.clearfix:before,
.clearfix:after {
  content: ".";    
  display: block;    
  height: 0;    
  overflow: hidden;
}
.clearfix:after {
  clear: both;
}
.clearfix {
  zoom: 1;
}
```
方案二
``` CSS
.clearfix:before, .clearfix:after {
  content:"";
  display:table;
}
.clearfix:after{
  clear:both;
  overflow:hidden;
}
.clearfix{
  zoom:1;
}
```
