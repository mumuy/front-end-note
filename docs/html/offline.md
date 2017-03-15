### 离线存储
HTML5的离线存储使用一个manifest文件来标明哪些文件是需要被存储的
```html
<html manifest='offline.manifest'>
```

offline.manifest文件内容
```html
<mime-mapping>
    <extension>manifest</extension>
    <mime-type>text/cache-manifest</mime-type>
</mime-mapping>
```  