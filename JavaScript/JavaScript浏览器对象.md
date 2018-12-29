# JavaScript浏览器对象

## window对象

1. window对象：

   window对象是BOM的核心，window对象指当前的浏览器窗口

   所有JavaScript全局对象、函数以及变量均自动成为window对象成员

   全局变量都是window对象的属性

   全局函数是window对象的方法

   甚至HTML DOM的document也是window对象的属性之一

2. window尺寸

   window.innerHeight - 浏览器窗口的内部高度

   window.innerWidth - 浏览器窗口的内部宽度

3. window方法啊

   window.open() - 打开新的窗口

   window.close() - 关闭当前窗口

```html
<button id="btn" onclick="btnClicked()">按钮</button>
    <script>
        window.document.write("宽度：" + window.innerWidth + "高度：" + 				 window.innerHeight);

        function btnClicked() {
            //window.open("newIndex.html", "windowName", "height = 200, width = 200, toolbar = no");
            window.close();
        }
    </script>
```

## 计时器对象

1. 计时事件：

   通过使用JavaScript,我们有能力做到在一个设定的时间间隔之后再来执行代码，而不是在函数被调用以后立即执行，我们称之为计时事件。

2. 计时方法：

   * **setInterval()**：间隔指定的毫秒数不停地执行指定的代码

     **clearInterval()**:方法用于停止setInterval()方法执行的函数代码

   ```html
       <p id="ptime">哈哈哈</p>
       <button id="btn" onclick="stopTime()">停止时间</button>
       <script>
           var myTime = setInterval(function () {
               getTime();
           }, 1000);
           function getTime() {
               var date = new Date();
               var t = date.toLocaleTimeString();
               document.getElementById("ptime").innerHTML = t;
           }
           function stopTime() {
               clearInterval(myTime);
           }
       </script>
   ```

   * **setTimeout()**:暂停指定的毫秒数后执行指定的代码

     **clearTimeout()**: 方法用于停止执行setTimeout()方法的函数代码(常用于递归循环，自己调自己)

```javascript
        var win;
        function myWin(){
            win = setTimeout(function () {
                alert("hello");
            }, 3000);               //在三秒钟后执行函数
        }
```

## History对象

1. History对象

   history.back() -与在浏览器点击后退按钮相同

   history.forward() -与在浏览器中点击向前按钮相同

   history.go() - 进入历史中的某个页面



## Location对象

1. Location对象

   `window.location`对象用于获得当前页面的地址（URL）,并把浏览器重新定向到新的页面。

2. Location对象的属性：

   `location.hostname`返回web主机的域名

   `location.pathname`返回当前页面的路径和文件名

   `location.port`返回web主机的端口

   `location.protocol`返回所使用的web协议（http://或者https://）

   `location.href`属性返回当前页面的URL

   `locaiotn.assign()`加载新的文档

```:zambia:
window.location.hostname
```

