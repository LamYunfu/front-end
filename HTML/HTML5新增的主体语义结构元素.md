# HTML5新增的主体语义结构元素

## 为何使用 HTML5 元素？

如果使用 HTML4 的话，开发者会使用他们喜爱的属性名来设置页面元素的样式：

header, top, bottom, footer, menu, navigation, main, container, content, article, sidebar, topnav, ...

如此，浏览器便无法识别正确的网页内容。

而通过 HTML5 元素，比如：<header> <footer> <nav> <section> <article>，此问题迎刃而解。

根据 W3C，语义网：

> “允许跨应用程序、企业和团体对数据进行分享和重用。

## 什么是语义元素？

语义元素清楚地向浏览器和开发者描述其意义。

*非语义*元素的例子：<div> 和 <span> - 无法提供关于其内容的信息。

*语义*元素的例子：<form>、<table> 以及 <img> - 清晰地定义其内容。

---



### article元素

`<article> `元素规定独立的自包含内容。


文档有其自身的意义，并且可以独立于网站其他内容进行阅读。

`<article>` 元素的应用场景：


- 论坛
- 博客
- 新闻
- 内嵌页面

```html
<body>
    <article>
        <header>
            <h1>中国海洋大学</h1>
            <p>Hello,欢迎来到中国海洋大学</p>
        </header>
        <article>                       <!--嵌套-->
            <header>作者</header>
            <p>评论</p>
            <footer>底部</footer>
        </article>
        <footer>
            <p>这是底部</p>
        </footer>
    </article>

    <!--article表示插件-->
    <article>
        <h1>这是一个内嵌页面</h1>
        <object>
            <embed src="#" width="600" height="400">
        </object>
    </article>
</body>
```

### section元素

section元素用于对网站或应用 程序页面上的内容进行分块。一个section元素通常由内容以及标题组成。但是section元素并非一个普通的容器元素；当一个容器需要直接被定义成样式或通过脚本定义行为的时候，推荐使用div而不是section元素。section元素是必须要存在一个标题的，不要为没有标题的块使用section元素。

```html
 <article>
        <h1>苹果</h1>
        <p>这是一个苹果，很好吃，而且可以吃</p>
        <section>
            <h2>红富士</h2>
            <p>这是一种外表很红的苹果，吃起来也不错</p>
        </section>
        <section>
            <h2>国光</h2>
            <p>这是一种外表看起来一般的苹果，但是吃起来也不错</p>
        </section>
    </article>
```

### nav元素

`<nav> `元素定义导航链接集合。

`<nav> `元素旨在定义大型的导航链接块。不过，并非文档中所有链接都应该位于 `<nav> `元素中！


nav元素应用场景：

* 传统导航条
* 侧边栏导航
* 页内导航
* 翻页操作

```html
<body>
    <nav>
        <ul>
            <li><a href="#">主页</a> </li>
            <li><a href="#">开发文档</a> </li>
        </ul>
    </nav>
    <article>
        <header>
            <h1>html5和css3的历史</h1>
            <nav>
                <ul>
                    <li><a href="#">HTML5历史</a> </li>
                    <li><a href="#">CSS3历史</a> </li>
                </ul>
            </nav>
        </header>
        <section>
            <h1>HTML5历史</h1>
            <p>......</p>
        </section>
        <section>
            <h1>CSS3历史</h1>
            <p>......</p>
        </section>
        <footer>
            <a href="#">删除</a>
            <a href="#">修改</a>
        </footer>
    </article>
<footer>
    <p><small>版权声明</small></p>
</footer>
</body>
```

### aside元素

`<aside> `元素页面主内容之外的某些内容（比如侧栏）。


aside 内容应该与周围内容相关。它可以包含与当前页面或者主要内容相关的引用、侧边栏、广告、导航条，以及其它类似的区别于主要内容的部分。

```html
<article>
    <h1>语法</h1>
    <p>文章的正文。。。</p>
    <aside>
        <h1>名词解释</h1>
        <p>语法：这是对于一个语言来说非常重要的部分</p>
    </aside>
</article>
```

### header元素

<header> 元素为文档或节规定页眉。

<header> 元素应该被用作介绍性内容的容器。

一个文档中可以有多个 <header> 元素。

```html
<!--html4写法-->
    <div class="header"></div>
    <div class="content"></div>
    <div class="footer"></div>
<!--html5写法-->
    <header>
        <h1>IT最新技术</h1>
        <a href="http://www.csdn.com" target="_self">CSDN</a>
        <nav>
            <ul>
                <li><a href="#">学习</a> </li>
                <li><a href="#">技术</a> </li>
                <li><a href="#">蓝云甫</a> </li>
            </ul>
        </nav>
    </header>
    <article></article>
    <footer></footer>
```



### footer元素

<footer> 元素为文档或节规定页脚。

<footer> 元素应该提供有关其包含元素的信息。

页脚通常包含文档的作者、版权信息、使用条款链接、联系信息等等。

```html
<!--html5之前的书写方式-->
    <div class="footer">
        <ul>
            <li><a href="#">版权信息</a></li>
            <li><a href="#">站点地图</a></li>
            <li><a href="#">联系方式</a></li>
        </ul>
    </div>
    <!--html5方式-->
    <footer>
        <ul>
            <li><a href="#">版权信息</a></li>
            <li><a href="#">站点地图</a></li>
            <li><a href="#">联系方式</a></li>
        </ul>
    </footer>
```

### hgroup元素

hgroup元素是将标题及其子标题进行分组的元素。hgroup元素通常会将h1~h6元素进行分组，譬如一个内容区块的标题及其子元素算一组。

```html
<article>
    <header>
        <hgroup>
            <h1>这是文章标题</h1>
            <h2>这是一个子标题</h2>
        </hgroup>
        <p>
            <time datetime="2018-10-28">2018-10-28</time>
        </p>
    </header>
</article>
```

### address元素

用于定义开发者联系信息等

```html
<address>
    <a href="#">lucas</a>
</address>
```

