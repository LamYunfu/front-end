# JavaScript DOM对像

## DOM简介

当网页被加载的时候，浏览器会创建页面的文档对象模型（Document Object Model）

1. DOM操作HTML
   1. JavaScript能改变页面中的所有HTML元素
   2. JavaScript能改变页面中的所有HTML属性
   3. JavaScript能改变页面中的所有CSS样式
   4. JavaScript能改变页面中的所有事件做出反应

## DOM操作HTML

1. 改变HTML输出流

   注意：绝对不要在文档加载完成之后使用document.write()。这会覆盖原来的文档。

2. 寻找元素：

   通过id找到HTML元素

   ```javascript
   document.getElementById("pid");
   ```

   通过标签名找到HTML元素

   ```javascript
   document.getElementByTagName("p");		//如果有两个p元素，会寻找当匹配的第一个p元素
   ```

3. 改变HTML内容:

   使用属性：innerHTML

   ```javascript
   var nv = document.getElementById("pid");
   nv.innerHTML = "World";
   ```

4. 改变HTML属性：

   使用属性：attribute

   ```html
   <a id="aid" href="http://baidu.com"> Hello </a>
   <script>
       function demo(){
           document.getElementById("aid").href="http://www.hao123.com";
       }
   </script>
   ```

## DOM操作CSS

语法：

```javascript
document.getElementById(id).style.property=new style
```

例子：

```html
<div class="div" id="div">
    Hello
</div>
<button onclick="demo()">按钮</button>
<script>
    function demo(){
        document.getElementById("div").style.background="blue";
    }
</script>
```

```css
.div{
    height: 100px;
    width: 100px;
    background-color: red;
}
```



## DOM EventListner

1. 方法：

   * addEventListner()			方法用于向指定元素添加句柄

   ```html
   <p id="pid"> hello </p>
   <button id="btn"></button>
   <script>
       document.getElementById("btn").addEventListener("click",function () {
           alert("hello");
       });				//使用匿名函数，避免了更改函数时需要更改两处
       
       var x = document.getElementById("btn");
       x.addEventListner("click",hello);
       x.addEventListner("click", world);
       x.removeEventListner("click", hello);
       
       function hello(){
           alert("hello");
       }
       function world(){
           alert("world");
       }
   </script>
   ```

   添加的句柄不会覆盖，都会显示

   * removeEventListner()                    移除方法添加的事件句柄

## 事件对象

在触发DOM事件的时候都会产生一个对象

事件对象的event：

1. type:获取事件类型
2. target:获取事件目标
3. stopPropagation(): 阻止事件冒泡
4. preventDefault()：阻止事件默认行为

```html
<script>
        document.getElementById("btn1").addEventListener("click", showType);
        document.getElementsById("aid").addEventListener("click", showA);
        function showType(event){
            alert(event.type);
            alert(event.target);
        }
        function showA(event){
            event.preventDefault();     //阻止默认事件的执行
        }
</script>
```

