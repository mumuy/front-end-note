禁用鼠标
``` CSS
pointer-events: none;
```

禁止文本选中
``` CSS
-moz-user-select: none;
-webkit-user-select: none;
-ms-user-select: none;
-khtml-user-select: none;
user-select: none;
```

自定义文本选择
``` CSS
::selection { background: #e2eae2; }
::-moz-selection { background: #e2eae2; }
::-webkit-selection { background: #e2eae2; }
```

禁用输入法
``` CSS
ime-mode:disabled;
```

隐藏IE10默认在input框输入内容后显示“X”按钮
``` CSS
pointer-events: none;
```
