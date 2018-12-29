# JavaScript事件

| 事件        | 描述             |
| ----------- | ---------------- |
| onClick     | 单击事件         |
| onMouseOver | 鼠标经过事件     |
| onMouseOut  | 鼠标移出事件     |
| onChange    | 文本内容改变事件 |
| onSelect    | 文本框选中事件   |
| onFocus     | 光标聚集事件     |
| onBlur      | 移开光标事件     |
| onLoad      | 网页加载事件     |
| onUnload    | 关闭网页事件     |

```html
<body onload="mgs()">
    <button onclick="demo()">按钮</button>
    <script>
        function demo(){
            alert("哈哈哈");
        }
    </script>

    <div class="div" onmouseover="mouseOver(this)" onmouseout="mouseOut(this)"></div>
    <script>
        function mouseOver(ooj){
            ooj.innerHTML = "hello";
        }
        function mouseOut(ooj){
            ooj.innerHTML = "world";
        }
    </script>

    <form>
        <input type="text" onchange="change(this)">
        <input type="text" onselect="select(this)">
    </form>
    <script>
        function change(ooj){
            alert("内容发生改变");
        }
        function select(ooj){
            ooj.style.backgroundColor = "blue";
        }
        function mgs() {
            alert("网页内容加载完毕")；
        }
    </script>


</body>
```

## 事件流

描述的是在页面中接收事件的顺序

1. 事件冒泡:

   由最具体的元素接收，然后逐级向上传播至最不具体的元素的节点（文档）

2. 事件捕获:

   最不具体的元素先接收事件，而最具体的节点应该是最后接收事件

## 事件处理

1. HTML事件处理：

   直接添加到HTML结构当中去

2. DOM0级事件处理

   把一个函数赋值给一个事件处理程序属性

3. DOM2级事件处理

   addEventListner("事件名"，”事件处理函数“，”布尔值“)；

   true: 事件捕获

   false: 事件冒泡

   removeEventListner();

4. IE事件处理程序：

   attachEvent

   detachEvent

```html
<body>
    <div id="div">
        <button id="btn1" onclick="demo()">按钮</button>
    </div>
    <script>
        function demo(){
            alert("HTML事件处理");
        }
    </script>
    <script>
        var btn1 = document.getElementById("btn1");
        btn1.click() = function () {
            alert("DOM0级事件处理");             //事件会被覆盖
        }
    </script>
    <script>
        var btn1 = document.getElementById("btn1").addEventListener("click",function () {
            alert("DOM2级事件处理程序");           //事件不会覆盖
        });
    </script>
</body>
```

## 事件对象

在触发