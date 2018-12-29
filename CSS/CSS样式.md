# CSS样式

## CSS背景

1. 背景：

   * CSS允许应用纯色作为背景，也允许使用背景图像创建相当复杂的效果

   | 属性                  | 描述                                       |
   | --------------------- | ------------------------------------------ |
   | background-attachment | 背景图像是否固定或者随着页面的其余部分滚动 |
   | background-color      | 设置元素的背景颜色                         |
   | backgroung-image      | 把图片设置为背景                           |
   | background-position   | 设置背景图片的起始位置                     |
   | background-repeat     | 设置背景图片是否及如何重复                 |

```css
body{
    background-color: antiquewhite;
    background-image: url("120725003.jpg");
    background-repeat: no-repeat;
    background-position: center top;    /*页面开始显示位置，图片开始显示位置*/
    background-attachment: fixed;
}
```

2. CSS3背景

* background-size:规定背景图片的尺寸
* background-origin:规定背景图片的定位区域
* background-clip:规定背景的绘制区域

## CSS文本

* CSS文本属性可以定义文本外观
* 通过文本属性，可以改变文本的颜色、字符间距、对齐文本、装饰文本、对文本进行缩进

| 属性            | 描述                 |
| --------------- | -------------------- |
| color           | 文本颜色             |
| direction       | 文本方向             |
| line-height     | 行高                 |
| letter-spacing  | 字符间距             |
| text-align      | 对齐元素中的文本     |
| text-decoration | 向文本添加修饰       |
| text-indent     | 缩进文本中元素的首行 |
| text-transfrom  | 元素中的字母         |
| unicode-bidi    | 设置文本方向         |
| white-space     | 元素中空白的处理方式 |
| word-spacing    | 字间距               |

```css
body{
    color: chartreuse;
    text-align: right;      /*向右对齐*/
}
div{
    text-align: left;
    color: black;
}
h3{
    text-indent: 2em;       /*首行缩进两格*/
}
#p1{
    text-transform: capitalize;         /*所有单词首字母大写*/
}
#p2{
    text-transform: lowercase;          /*所有字母小写*/
}
```

* CSS3文本效果：
  * text-shadow:向文本添加阴影
  * word-wrap:规定文本的换行规则

---

## CSS字体

| 属性         | 描述                                 |
| ------------ | ------------------------------------ |
| font-family  | 字体系列                             |
| font-size    | 字体的尺寸                           |
| font-style   | 字体风格                             |
| font-variant | 以小型大写字体或者正常字体来显示文本 |
| font-weight  | 字体的粗细                           |

## CSS链接

1. CSS链接的四种状态：

   **a:link**	普通的、未被访问的链接

   **a:visited**	用户已访问的链接

   **a:hover**		鼠标指针位于链接的上方

   **a:active** 	链接被点击的时刻

2. 常见的链接样式：

   text-decoration属性大多用于去掉链接中的下划线

   `text-decoration: none;`

## CSS列表

* CSS列表属性允许你放置、改变列表标志，或者将图像作为列表的标志

| 属性               | 描述         |
| ------------------ | ------------ |
| list-style         | 简写列表项   |
| list-style-image   | 列表项图像   |
| list-style-positon | 列表标志位置 |
| list-style-type    | 列表类型     |

> Class和id的区别：class可以重复，id必须唯一
>
> 加载方式：id先找到结构内容，再加加载样式；class先加载样式，再加载具体内容

## CSS表格

CSS表格属性可以帮助我们极大的改善表格的外观

1. 表格边框
2. 折叠边框
3. 表格宽高
4. 表格文本对齐
5. 表格内边距
6. 表格颜色

```css
#tb,tr,th,td{
    border: 1px solid blue;
    text-align: center;				/*文字居中*/

}
#tb{
    width: 400px;
    height: 400px;
    border-collapse: collapse;      /*边框折叠*/

}
```

## CSS轮廓

轮廓主要是用来突出元素的作用

| 属性          | 描述 |
| ------------- | ---- |
| outline       |      |
| outline-color |      |
| outline-style |      |
| outline-width |      |

```css
p{
    outline-style: groove;
    outline-width: 5px;
}
```

