### 去除表单自动填充颜色(Chrome浏览器)
``` CSS
input:-webkit-autofill {
  background-color: #FAFFBD;
  background-image: none;
  color: #000;
}
```

### 去除按键圆角(iPhone)
``` CSS
-webkit-appearance:none;
```

### 去除搜索按键(Chrome浏览器)
``` CSS
input[type="search"]::-webkit-search-cancel-button,input[type="search"]::-webkit-search-decoration{
  -webkit-appearance: none;
}
```

### 去除数字输入框增减按键(Chrome浏览器)
``` CSS
input[type="number"]::-webkit-outer-spin-button,input[type="number"]::-webkit-inner-spin-button{
  -webkit-appearance: none;
}
```

### 去除date类型文本框多了个叉叉清除内容的效果(Chrome浏览器)
``` CSS
::-webkit-clear-button {
    -webkit-appearance: none;
 }
 ```

### 去除按键虚线框(Firefox浏览器)
``` CSS
button::-moz-focus-inner,input::-moz-focus-inner{

}
```

### 改变password类型input框的默认样式(IE浏览器)
``` CSS
::-ms-reveal{display: none; }
::-ms-reveal{background-color:#f0f3f9; }
```

### 设置默认线框距离
``` CSS
input {outline-offset: 4px ;}
```

### input字体垂直居中
``` CSS
font-family:  Tahoma,Arial, Helvetica,"Microsoft YaHei";
```
