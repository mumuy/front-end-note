### 模糊
```css
-webkit-filter:blur(5px);
```

### 叠加褐色
取值范围0-1，此处表示50%的褐色
```css
-webkit-filter:sepia(0.5);
```

### 亮度
取值范围0-1，5倍亮度（数字为0时为正常样式，为1时表示的是100%亮度，无法看到图片）
```css
-webkit-filter:brightness(0.5);
```

### 色相
按照色相环进行旋转，顺时针方向，红-橙-黄-黄绿-绿-蓝绿-蓝-蓝紫-紫-紫红-红
```css
-webkit-filter:hue-rotate(30deg);
```

### 反色
取值范围0-1,0为原图，1为彻底反色之后，0.5为灰色
```css
-webkit-filter:invert(1);
```

### 饱和度
取值范围0~*,0为无饱和度，1为原图，值越高饱和度越大
```css
-webkit-filter:saturate(4);
```

### 对比度
取值范围0~*,0为无对比度（灰色），1为原图，值越高对比度越大
```css
-webkit-filter:contrast(2);
```

### 透明度
取值范围0~1,0为全透明，1为原图
```css
-webkit-filter:opacity(0.8);
```

### 阴影
```css
-webkit-filter:drop-shadow(17px 17px 20px black);
```