# CSS盒子模型

![1541419058826](C:\Users\蓝云甫\AppData\Roaming\Typora\typora-user-images\1541419058826.png)

### 概述

盒子模型的内容包括： margin、border、padding、content部分组成

### CSS内边距（padding）

CSS内边距在content外、边框border内

内边距属性有：

| 属性           | 描述         |
| -------------- | ------------ |
| padding        | 设置所有边距 |
| padding-bottom | 设置底部边距 |
| padding-left   | 设置左边距   |
| padding-right  | 设置右边距   |
| padding-top    | 设置上边距   |

```css
td{
    padding-bottom: 50px;
    padding-left: 20px;
    padding-right: 100px;
    padding-top: 10px;
}
```

![1541419755785](C:\Users\蓝云甫\AppData\Roaming\Typora\typora-user-images\1541419755785.png)

### CSS边框（border）

1. 我们可以创造出效果出色的边框，并且可以应用于任何元素

2. 边框的样式

* **border-style**:定义了10个不同的非继承样式，包括none

3. 边框的单边框样式
   * border-top-style
   * border-left-sytle
   * border-right-style
   * border-bottom-style 
4. 边框宽度  **border-width**
5. 边框单边宽度：
   * border-top-width
   * border-left-width
   * border-right-width
   * boder-bottom-width
6. CSS3边框
   * boder-radius: 圆角边框
   * box-shadow:边框阴影
   * border-image:边框图片

```css
p{
    border-top-style: dotted;
    border-left-style: solid;
    border-right-style: outset;
    border-bottom-style: groove;
    border-top-color: red;
    border-width: 10px;
}
```

### CSS外边距margin

外边距margin位于边框border之外属性类似于border,这里不做过多介绍（其实是懒）

### 外边距合并

外边距合并就是一个叠加的概念

比如，两个相邻的div都设置了margin属性，一个为100px，一个为50px,那在两个div相邻的部分不是150px，而是100px, 这是因为这两个外边距发生了外边距合并的现象，在合并的过程中取那个更大的外边距。

### 盒子模型实际应用项目

* html

```html
<body>
    <div class="top">
        <div class="top_content"></div>
    </div>
    <div class="body">
        <div class="body_image"></div>
        <div class="body_content">
            <div class="body_notification"></div>
        </div>
    </div>
    <div class="footing">
        <div class="footing_content"></div>
        <div class="footing_menu"></div>
    </div>
</body>
```

* css

```css
*{
    margin: 0px;
    padding: 0px;
}
.top{
    width: 100%;
    height: 50px;
    background-color: black;
}
.top_content{
    width: 75%;
    height: 50px;
    margin: 0px auto;   /*上下为0px，左右自适应有一个居中的效果*/
    background-color: cornflowerblue;
}
.body{
    margin: 20px auto;
    width: 75%;
    height: 1500px;
    background-color: cornsilk;
}
.body_image {
    width: 100%; /*宽度充满body的100%，也就是整体的75%*/
    height: 400px;
    background-color: coral;
}
.body_notification{
    width: 100%;
    height: 50px;
    background-color: cornflowerblue;
}
.body_content{
    width: 100%;
    height: 1100px;
    background-color: chartreuse;
}
.footing{
    width: 75%;
    height: 330px;
    background-color: darkorange;
    margin: 0px auto;
}
.footing_content{
    width: 100%;
    height: 280px;
    background-color: firebrick;
}
.footing_menu{
    width: 100%;
    height: 50px;
    background-color: pink;
}
```

* 实际效果

![1541492660054](C:\Users\蓝云甫\AppData\Roaming\Typora\typora-user-images\1541492660054.png)