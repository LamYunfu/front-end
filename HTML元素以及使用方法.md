# HTML元素以及使用方法

### HTML元素

注释方法`Ctrl + shift + /`

1. 元素是指从开始标签到结束标签的所有代码

`<br/>`表示换行

2. 嵌套的HTML元素

   大多数的HTML元素都是可以嵌套的。

3. 

## HTML属性

1. 标签可以拥有属性为元素提供更多的信息

2. 属性可以以键值对的形式出现

   如：`href="www.baidu.com"`

3. 常用的标签属性

   <h1>:align对齐方式

   <body>:bgcolor背景颜色

   <a>:target规定在何处打开链接

4. 通用属性

   class: 规定元素的类名

   id: 规定元素的唯一ID

   style: 规定元素的样式

   title: 规定元素的额外信息

## HTML格式化

| 标签     | 描述         |
| -------- | ------------ |
| <b>      | 定义粗体文本 |
| <big>    | 定义大号字   |
| <em>     | 定义着重文字 |
| <i>      | 定义斜体字   |
| <small>  | 定义小号字   |
| <strong> | 定义加重语气 |
| <sub>    | 定义下标字   |
| <sup>    | 定义上标字   |
| <ins>    | 定义插入字   |
| <del>    | 定义删除字   |

```html
	<b>欢迎来到王者荣耀</b>    <!-- 加粗 -->
    <br/>
    <big>欢迎来到王者荣耀</big>
    <br/>
    <em>定义着重字</em>
    <br/>
    <i>定义斜体字</i>
    <br/>
    <small>定义小号字</small>
    <br/>
    <strong>加重语气</strong>
    <br/>
    欢心<sub>上标</sub>西递
    <br/>
    欢心<sup>下标</sup>洗涤
    <br/>
    <ins>插入字</ins>
    <br/>
    <del>删除字</del>
    <br/>
```

## HTML样式

1. 标签

* <style>:样式定义
* <link>:资源引用

2. 属性

   rel = "stylesheet":外部样式表

   type = "text/css":引入文档类型

   margin-left: 边距

3. 三种插入样式的方式

* 外部样式表

  `<link rel="stylesheet" type="text/css" href="mystyle.css">`

* 内部样式表

  ```html
  <style type="text/css">
          p{
              color: cadetblue;
          }
  </style>
  ```

* 内联样式表

  `<p style = "color": red>`

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>样式</title>
    <link rel="stylesheet" type="text/css" href="mystyle.css">
    <style type="text/css">
        p{
            color: cadetblue;
        }
    </style>
</head>
<body>
    <h1>标题h1</h1>

    <p>欢迎来到王者荣耀</p>

    <a href="http://www.baidu.com" style = "color: maroon">点击我跳转到百度</a>
</body>
</html>
```



## HTML链接

1. 链接数据

   文本链接

   图片链接

2. 属性

   href属性：指向另一个文档的链接

   name属性：创建文档内的链接		//点击自动跳转到页面的该名字的位置，常见于网站的跳转到顶部

3. img标签属性：

   ​	alt: 替换文本属性，图片显示不出来时替换成相应的文本

   ​	width: 宽度

   ​	height: 高度

```html
<body>
    <a href="http://www.baidu.com">百度一下</a>
    <br/>
    <a href="http://www.baidu.com">
        <img src="Airwaves_109951163053001565.jpg" width="200px" height="200px" alt="htmlLogo">
    </a>
    <br/>
    <a name="tips">hello</a>
    <br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/>
    <a href="#tips">跳转到hello</a>
</body>
```



## HTML表格

| 表格      | 描述             |
| --------- | ---------------- |
| <table>   | 定义表格         |
| <caption> | 定义表格标题     |
| <th>      | 定义表格的表头   |
| <tr>      | 定义表格的行     |
| <td>      | 定义表格的单元   |
| <thead>   | 定义表格的页眉   |
| <tbody>   | 定义表格的主体   |
| <tfoot>   | 定义表格的页脚   |
| <col>     | 定义表格的列属性 |

## HTML列表

| 标签 | 描述                |
| ---- | ------------------- |
| <ol> | 有序列表（点代替)   |
| <ul> | 无序列表（1、2、3） |
| <li> | 无序列表列表项      |
| <dl> | 无前缀列表声明      |
| <dt> | 列表项              |
| <dd> | 描述                |

1. 无序列表

   使用标签：<ul>、<li>

   属性：type = disc、cicle、square，表示无序列表序号位置的形状，默认是disc

2. 有序列表

   使用标签：<ol>、<li>

   属性:type =  A a I i start

3. 嵌套列表

   使用标签：<ul> <ol> <li>

4. 自定义列表

   使用标签: <dl> <dt> <dd>

```html
<body>
    <!--无序列表-->
    <ul type="circle">
        <li>ios</li>
        <li>android</li>
        <li>html5</li>
        <li>swift</li>
    </ul>

    <!--有序列表-->
    <ol type="i">
        <li>ios</li>
        <li>android</li>
        <li>html5</li>
        <li>swift</li>
    </ol>

    <!--无序嵌套列表-->
    <ul>
        <li>宠物</li>
            <ul>
                <li>猫</li>
                <li>狗</li>
            </ul>
        <li>人类</li>
            <ul>
                <li>亚洲人</li>
                <li>非洲人</li>
            </ul>
        <li>植物</li>
            <ul>
                <li>花</li>
                <li>草</li>
            </ul>
    </ul>

    <!--有序嵌套列表-->
    <ol>
        <li>宠物</li>
        <ol>
            <li>猫</li>
            <li>狗</li>
        </ol>
        <li>人类</li>
        <ol>
            <li>亚洲人</li>
            <li>非洲人</li>
        </ol>
        <li>植物</li>
        <ol>
            <li>花</li>
            <li>草</li>
        </ol>
    </ol>

    <!--无前缀列表声明-->
    <dl>
        <dt>helloworld</dt>
            <dd>每一门新的语言都会打印hello world</dd>
        <dt>helloworld</dt>
            <dd>每一门新的语言都会打印hello world</dd>
        <dt>helloworld</dt>
            <dd>每一门新的语言都会打印hello world</dd>
        <dt>helloworld</dt>
            <dd>每一门新的语言都会打印hello world</dd>
    </dl>
</body>
```

---

## HTML块

1. HTML块元素

   块元素在显示的时候，通常会以新行开始

   如：<p>、<h1>

2. HTML的内联元素

   内联元素通常不会以新行开始

   如：<b>、<a>、<img>

3. HTML的 div 元素

   <div>元素也被称为块元素，其主要是组合HTML元素的容器

4. HTML的 span 元素

   <span>元素是内联元素，可以作为文本的容器, 主要用于对文本施加某种效果。

```html
<body>
    <!--自动换行的块-->
    <p>大家好</p>
    <h1>标题</h1>

    <!--内联元素-->
    <b>这是一个加重标签</b>
    <a>这个标签不会换行</a>

    <!--div元素-->
    <div id="divid">
        <a href="http://www.baidu.com">百度一下</a>
        <p>p标签段落</p>
    </div>

    <!--span元素-->
    <div id="divspan">
        <p><span>这是一个测试效果</span>span是一个什么样子</p>
    </div>
</body>
```

## HTML布局

1. 使用<div>元素布局
2. 使用<table>元素布局

```html
<style type="text/css">
        body{
            margin: 0px;
        }
        #container{
            width: 100%;
            height: 950px;
            background-color: azure;
        }
        #header{
            width:100%;
            height: 10%;
            color: coral;
        }
        #content_menu{
            width:30%;
            height:80%;
            background-color: darkorange;
            float:left;
        }
        #content_body{
            width:70%;
            height: 80%;
            background-color: brown;
            float:left;
        }
        #footing{
            width: 100%;
            height: 10%;
            background-color: chartreuse;
            clear: both;
        }
    </style>
</head>
<body>
    <div id="container">
        <div id="header">头部</div>
        <div id="content_menu">内容菜单</div>
        <div id="content_body">内容主体</div>
        <div id="footing">底部</div>
    </div>
</body>
```



```html
<body>
    <table width="100%" height="600px" style="color: chartreuse;">
        <tr>
            <td colspan="2" width="100%" height="10%" style="background-color: maroon">这是头部</td>
        </tr>
        <tr>
            <td width="30%" height="80%" style="background-color: blue">
                左菜单
                <ul>
                    <li>android</li>
                    <li>ios</li>
                    <li>html</li>
                </ul>
            </td>

            <td width="70%" height="80%" style="background-color: purple">右菜单</td>
        </tr>
        <tr>
            <td width="100%" height="10%" colspan="2" style="background-color: crimson">这是底部</td>
        </tr>
    </table>
</body>
```

## HTML表单

```html
<body>
    <form>
        用户名：
        <input type="text">
        <br/>
        密码：
        <input type="password">
        <br/>
        <!--复选框-->
        你喜欢的水果有：
        <br/>
        苹果<input type="checkbox">
        西红柿<input type="checkbox">
        香蕉<input type="checkbox">
        <!--单选框-->
        <br/>
        请选择你的性别：
        男<input type="radio" name="gender">
        女<input type="radio" name="gender">         <!--gender用于将两个元素集合在一起，实现单选的效果-->
        <br/>
        <!--下拉列表-->
        请选择您常用的网站：
        <select>
            <option>www.baidu.com</option>
            <option>www.google.com</option>
            <option>www.taobao.com</option>
        </select>
        <br/>
        <!--文本域-->
        <textarea cols="30" rows="30">请在此添加您的个人信息</textarea>
        <br/>
        <!--按钮-->
        <input type="button" value="提交">
    </form>
</body>
```

