### 文档视图
``` javascript
var element = document.elementFromPoint(100,100);
//返回给定坐标处所在的元素
```

### 元素视图
``` javascript
var data = element.getBoundingClientRect()
//得到矩形元素的界线，返回的是一个对象，包含 top, left, right, 和 bottom四个属性值，大小都是相对于文档视图左上角计算而来

var data = element.getClientRects()
//返回元素的数个矩形区域，返回的结果是个对象列表，具有数组特性。这里的矩形选区只针对inline box，因此，只针对a, span, em这类标签元素

element.scrollIntoView()
//将对象滚动到可见范围内,将其排列到窗口顶部或底部（不属于草案方法）
```