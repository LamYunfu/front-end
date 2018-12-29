# CSS常用操作

## 对齐操作

1. 使用margin属性进行水平对齐

```css
    margin-left: auto;
    margin-right: auto;
	margin: 0px auto;    /*上下外边距为0px，左右自适应居中*/
```

2. 使用position属性进行左右对齐

```css
position: absolute;
right: 0px;     /*居右对齐，元素向右偏移量为0px*/
left: 0px;      /*居左对齐*/
```

3. 使用float属性进行左右对齐

```css
float: left;
```

## 尺寸操作

1. 属性：

| 属性        | 描述           |
| ----------- | -------------- |
| height      | 设置元素高度   |
| line-height | 行高（行间距） |
| max-height  | 元素最大高度   |
| max-width   | 元素最大宽度   |
| min-height  |                |
| min-width   |                |
| width       | 元素宽度       |

* 行高

```css
#p1{
    width: 400px;
    line-height: normal;
}
#p2{
    width: 400px;
    line-height: 200px;
}
#p3{
    width: 400px;
    line-height: 50%;
}
```

![1541494448973](C:\Users\蓝云甫\AppData\Roaming\Typora\typora-user-images\1541494448973.png)

## 分类操作

1. 属性：

| 属性       | 描述                                                       |
| ---------- | ---------------------------------------------------------- |
| clear      | 设置一个元素的侧面是否允许其它的元素浮动                   |
| cursor     | 规定当光标指向该元素之上时显示的指针类型（箭头、小手指等） |
| display    | 设置是否以及如何显示元素（主要应用与列表中）inline         |
| float      | 定义元素在哪个方向浮动                                     |
| position   | 把元素放置在一个静态的、相对的、绝对的、固定的位置         |
| visibility | 设置元素是否可见（hidden\|visible）                        |

### 导航栏操作

垂直还是水平通过display属性来进行设置

1. 垂直导航栏		`display:block`
2. 水平导航栏             `display: inline`
3. 导航栏效果

```css
ul{
    list-style-type: none;
    margin: 0px;
    padding: 0px;

}
/*设置链接未被点击和访问过以后的样式*/
a:link,a:visited{
    text-decoration: none;          /*去掉下划线*/
    background-color: bisque;
    color: black;               /*文字颜色*/
    text-align: center;         /*文字居中*/
    width: 100px;
}
/*设置鼠标hover和点击时刻链接的样式*/
a:hover,a:active{
    background-color: red;
}
li{
    display:inline;
    padding: 3px, 3px;
    font-size: larger;          /*字体大小*/
    font-weight: 600;           /*文字变粗*/
}
```

## 图片

