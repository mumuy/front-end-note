Chrome浏览器(webkit)
``` CSS
::-webkit-input-placeholder {
  color: #999;
}
```
注：webkit下在文本框获取焦点后不显示placeholder，以便使其与其他浏览器表现一致
``` CSS
:focus::-webkit-input-placeholder {
  color: transparent !important;
}
```

Firefox浏览器
``` CSS
/* Mozilla Firefox 4 to 18 */
:-moz-placeholder {
  color: #999;
}
/* Mozilla Firefox 19+ */
::-moz-placeholder {
  color: #999;
}
```

IE浏览器
``` CSS
/* Internet Explorer 10+ */
:-ms-input-placeholder {
  color: #999;
}
```
