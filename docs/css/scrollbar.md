### 自定义滚动条
```css
::-webkit-scrollbar{width:12px;height:12px;}
::-webkit-scrollbar-button:start:decrement, ::-webkit-scrollbar-button:end:increment{width:0;height:0;}
::-webkit-scrollbar-button:vertical:increment{background:transparent;}
::-webkit-scrollbar-track-piece:vertical{background:#DFE7EF;}
::-webkit-scrollbar-track-piece:vertical:hover{background:#DFE7EF;}
::-webkit-scrollbar-track-piece:horizontal{background-color:transparent;}
::-webkit-scrollbar-thumb:vertical{height:100px;background:rgba(110,146,182,.5);}
::-webkit-scrollbar-thumb:vertical:hover{background:rgba(110,146,182,.4);}
::-webkit-scrollbar-thumb:horizontal{width:80px;height:10px;background-color:#ccc;}
```

### iOS自定义滚动条兼容
```css
-webkit-overflow-scrolling:touch;		/* 惯性 */
-webkit-transform:translate3d(0,0,0);	/* 下滑卡顿并出现空白 */
```