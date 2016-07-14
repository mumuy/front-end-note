方法一
```javascript
var isSupported = CSS.supports("display", "flex");
```
方法二
```javascript
var isSupported = CSS.supports("(display: flex) and (-webkit-appearance: caret)");
```

### 兼容写法
```javascript
var supportsCSS = !!((window.CSS && window.CSS.supports) || window.supportsCSS || false);
```