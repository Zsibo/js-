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



## 自定义属性设置、获取、移除

设置自定义属性:`setAttribute("属性名字","属性值");` 

获取自定义属性:`getAttribute("属性名字");` 

移除自定义属性:`removeAttribute("属性名字");`  

移除元素类样式的值:`对象.className="";`  

`removeAttribute("属性名字")` 也可以移除元素的自带属性,`.className="";` 只是移除属性的值,属性还在

```javascript
my$("dv").setAttribute("score",100);  定义div的score属性为100
my$("dv").getAttribute("score");      获取div的score属性的值
my$("dv").removeAttribute("score");   移除div的score属性
my$("dv").className="";               移除div的class类样式的值
```

