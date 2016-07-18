### 禁用鼠标
``` CSS
pointer-events: none;
```

### 禁止文本选中
``` CSS
-moz-user-select: none;
-webkit-user-select: none;
-ms-user-select: none;
-khtml-user-select: none;
user-select: none;
```

### 禁用输入法
``` CSS
ime-mode:disabled;
```

### 禁用系统默认菜单
``` CSS
-webkit-touch-callout:none;
```

### 禁止触发鼠标或者触屏事件
``` CSS
pointer-events: none;
```

### 自定义文本选择
``` CSS
::selection { background: #e2eae2; }
::-moz-selection { background: #e2eae2; }
::-webkit-selection { background: #e2eae2; }
```