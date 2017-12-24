## innerHTML和innerText/outerHTML的区别

document对象中的`innerHTML` 和`innerText` 属性都是获取对象的文本内容的

```html
<html>  
    <head><title>innerHTML</title></head>  
    <body>  
        <div id="d1"><p id="p1">hello world </p></div>  
        <script>  
            var content = document.getElementById("d1");  
            alert(content.innerHTML);  
            alert(content.innerText);
        </script>  
    </body>  
</html>
```

通过IE浏览器打开,弹出内容为`<p id="p1">hello world </p>` 和`hello world` 

通过Firefox浏览器打开,弹出内容为`<p id="p1">hello world </p>` 和`undefind` 

通过chrome浏览器打开,弹出内容为`<p id="p1">hello world </p>` 和`hello world` 

`innerHTML` 指的是从对象的起始位置到终止位置的全部内容,包括html标签

`innerText` 指的是从对象的起始位置到终止位置的全部内容,但是它去除Html标签

`innerHTML` 标签是所有浏览器都支持的,`innerText` 是IE浏览器和chrome浏览器支持的,低版本Firefox浏览器不支持,但支持`textContent` 

`alert(content.outerHTML)` 浏览器弹出内容为`<p id="p1">hello world </p>` 和`<div id="d1"><p id="p1">hello world </p></div>` 

