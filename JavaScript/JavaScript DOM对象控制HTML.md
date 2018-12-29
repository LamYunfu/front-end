# JavaScript DOM对象控制HTML

## 方法

getElementByName()			---获取name

getElementByTagName()			--获取元素

getAttribute()					--获取元素属性

setAttribute()					--设置元素属性

childNodes()						--访问子节点

parentNode()					--访问父节点

createElement()					--创建元素节点

createTextNode()					--创建文本节点

insertBefore()					--插入节点

removeChild()					--删除节点

offsetHeight						--网页尺寸(不包含滚动条)

scrollHeight						--网页尺寸(包含滚动条)

```html
<body>
    <p name="pn">Hello</p>
    <p name="pn">Hello</p>
    <p name="pn">Hello</p>
    <p name="pn">Hello</p>
    <a id="aid" title="得到了a标签的属性">hello</a>
    <a id="aid2">aid2</a>

    <ul>
        <li>one</li><li>two</li><li>three</li>
    </ul>

    <div id="div">
        <p id="pid">div的p元素</p>
    </div>
    <script>
        function getName(){
            var count = document.getElementsByName("pn");
            var count1 = document.getElementsByTagName("p");  //获取的元素和上面是一样的
            var p = count[0];
            p.innerHTML = "World";
        }
        getName();

        //获取元素属性
        function getAttr() {
            var anode = document.getElementById("aid");
            var attr = anode.getAttribute("title");
            alert(attr);

        }
        getAttr();

        //设置元素属性和属性值
        function setAttr() {
            var anode = document.getElementById("aid2");
            anode.setAttribute("title", "动态设置a的title属性");
            var attr = anode.getAttribute("title");
            alert(attr);
        }
        setAttr();

        //访问子节点
        function getChildNode() {
            var childNode = document.getElementsByTagName("ul")[0].childNodes;  //获得第一个ul的子节点集合
            alert(childNode.length);            //空白项也算一项
        }
        getChildNode();

        //访问父节点
        function getParentNode(){
            var div = document.getElementById("pid");
            alert(div.parentNode.nodeName);
        }
        getParentNode();

        //创建结点,通过body.append()方法在body元素中追加节点
        function createNode() {
            var body = document.body;
            var input = document.createElement("input");  //输入标签名称
            input.type = "button";
            input.value = "按钮";
            body.appendChild(input);
        }
        createNode();

        //插入节点
        function addNode() {
            var div = document.getElementById("div");
            var node = document.getElementById("pid");
            var newNode = document.createElement("p");
            newNode.innerHTML="动态插入一个p元素";
            div.insertBefore(newNode, node);
        }
        addNode();

        //删除节点
        function removeNode(){
            var div = document.getElementById("div");
            var p = div.removeChild(div.childNodes[1]);
            alert("删除的结点是：" + p.innerHTML);
        }
        removeNode();

        //获得屏幕尺寸
        function getSize() {
            var width = document.body.offsetWidth;
            var height = document.body.offsetHeight;
            alert(width + "," + height);
        }
        getSize();
        
    </script>
</body>
```

