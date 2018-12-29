# JavaScript内置对象

## 创建对象的三种方式

```html
<body>
    <!--创建对象方式一-->
    <script>
        people = new Object();   //使用new Object()方式创建对象，object对象是所有对象的父类
        people.name = "lucas";      //通过对象.属性 = 属性值, 来给对象添加属性和属性值
        people.age = 20;
        document.write("name:" + people.name + " age:" + people.age);
    </script>
    <!--创建对象方式二-->
    <script>
        people = {name:"lucas", age:"30"};   //直接创建对象并初始化
        document.write(people.name);
    </script>
    <!--创建对象方式三，使用函数来定义对象，然后创建新的对象实例-->
    <script>
        function people(name, age){
            this.name = name;
            this.age = age;
        }
        son = new people("lucas", 30);
        document.write(son.name + " " + son.age);
    </script>
</body>
```

## String字符串对象

1. String对象

* String对象用于处理已有的字符串
* 字符串对象既可以使用单引号，也可以使用双引号

2. String字符串常用方法

   * 在字符串中查找某个特定的字符序列： `indexOf()`,如果存在该字符序列，那么就返回这个字符序列第一次出现的位置，如果不存在就返回-1。

   ```html
   	<script>
           var str = "Hello World";
           document.write("字符串长度"+ str.length + "</br>");
           document.write(str.indexOf("World"));
       </script>
   ```



   * 内容匹配：`match()`, 匹配一个字符序列在字符串中是否存在，如果存在，则直接返回该字符序列，如果不存在，则返回null。

     ```html
     <script>
     	var str = "Hello World";
         document.write(str.match("World"));
     </script>
     ```

   * 替换内容： `replace()`

     ```javascript
     str.replace("World","Lucas");			//把字符串中的World替换成Lucas
     ```

   * 字符串大小写转换：`toUpperCase()/toLowerCase()`
   * 将字符串转换为一个字符数组

   ```javascript
   var str1 = "hello,ouc,world";
   var s = str1.split(",");
   ```

   * ...

   ---

   ## Date日期对象

   日期对象主要用于操作日期和时间

   主要方法：

   ```html
       <script>
           var date = new Date();
           document.write(date.getFullYear());   //获取档当前年份
           document.write(date.getTime());       //获取当前毫秒数(从1970年开始算起)
           date.setFullYear(2000,1,1);            //设置时间
       </script>
   ```

   时钟实例：

   ```html
   <body onload="startTime()">         <!--在页面的加载之初就掉哦那个该函数-->
       <script>
           // var date = new Date();
           // document.write(date.getFullYear());   //获取档当前年份
           // document.write(date.getTime());       //获取当前毫秒数(从1970年开始算起)
           // date.setFullYear(2000,1,1);            //设置时间
           function startTime(){
               var today = new Date();
               var h = today.getHours();
               var m = today.getMinutes();
               var s = today.getSeconds();
               m = checkTime(m);
               s = checkTime(s);
               document.getElementById("clock").innerHTML = h + ":" + m + ":" + s;
               t = setTimeout(function(){
                   startTime();
               }, 1000);              //每延迟1000ms自动递归调用一次，实现时间的不断刷新
           }
           function checkTime(num){
               if(num < 10){
                   num = "0" + num;
               }
               return num;
           }
       </script>
       <div id="clock">
   
       </div>
   </body>
   ```

   ---

   ## Array数组对象

   1. Array数组对象：

      使用单独的变量名来存储一系列的值

   2. 数组的创建：

      `var myArray=["hello", "world", "bye"]`

   3. 数组常用方法：

      * `concat()`:合并数组
      * `sort()`:排序
      * `push()`:末尾追加元素
      * `reverse()`:数组元素翻转

   ```html
       <script>
           var arr1 = ["hello", "world"];
           var arr2 = ["lucas", "azul"];
           var c = arr1.concat(arr2);         //数组合并
           document.write(c + "<br/>");
   
           var arr3 = ["hello", "azul", "what", "you", "compromise"];
           document.write(arr3.sort() + "<br/>");            //按照字典顺序排序
           var arr4 = [2, 34, 66, 4, 35, 31, 20];
           document.write(arr4.sort(function (a, b) {
               return b - a;                               //按照降序排列
           }));
           
           var arr5 = ["a", "b"];
           arr5.push("c");             //在arr5之后追加c
           arr5.reverse();             //数组翻转
       </script>
   ```

   ## Math对象

   执行常用的算术任务

   常用方法：

   `round()`:四舍五入

   `max()`:返回最大值

   `random()`:返回0 - 1之间的随机数

   `min()`: 返回最低值

   `abs()`:返回绝对值