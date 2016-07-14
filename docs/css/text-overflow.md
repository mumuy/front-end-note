### 文本超出省略号
``` CSS
display:block;
overflow: hidden;
white-space: nowrap;
text-overflow: ellipsis;
```

### 多行文本超出省略号
``` CSS
display: -webkit-box;
-webkit-box-orient: vertical;
text-overflow: ellipsis;
overflow: hidden;
-webkit-line-clamp: 2;
```
