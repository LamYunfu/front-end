# CSS动画

## 2D、3D转换

1. 通过CSS3转化，我们能够对元素进行移动、缩放、转动、拉长或拉伸

   转换是使元素改变形状、尺寸和位置的一种效果

   可以使用2D、3D来转换元素

2. 2D转换方法

   translate()

   rotate()

   scale()

   matrix()

   ```css
   .div2{
       margin-top: 200px;
       transform: translate(100px, 100px);         /*x轴移动100px,Y轴移动100px*/
       -webkit-transform: translate(100px, 100px);     /*支持safari和chrome*/
       -ms-transform: translate(100px, 100px);         /*支持ie*/
       -o-transform: translate(100px, 100px);         /*支持opera*/
       -moz-transform: translate(100px, 100px);         /*支持firefox*/
   }
   
   .div2{
       -webkit-transform: rotate(180deg);              /*旋转180度*/
   }
   .div2{
       -webkit-transform: scale(1,2);              /*宽度缩放一倍，高度缩放两倍*/
   }
   .div{
       -webkit-transform: skew(50deg, 50deg);          /*绕X轴倾斜50度，绕Y轴倾斜50度*/
   }
   
   ```

3. 3D转换方法：

   rotateX()

   rotateY()

## 过渡

1. CSS3过渡元素是从一种样式转换成另外一种样式

   动画效果的CSS

   动画执行的时间

2. 属性：

| 属性                       | 描述                         |
| -------------------------- | ---------------------------- |
| transiton                  | 设置四个过渡属性             |
| transiton-property         | 过渡的名称                   |
| transtion-duration         | 过渡效果花费的时间           |
| transition-timing-function | 过渡效果的时间曲线           |
| transition-delay           | 过渡效果开始时间（延时时间） |

```css
div{
    width: 100px;
    height: 100px;
    background-color: darkorange;
    -webkit-transition: width 2s, height 2s, -webkit-transform 2s;
}
div:hover{
    width: 200px;
    height: 200px;
    -webkit-transform: rotate(360deg);
}
```

## 动画

CSS3动画需要遵循@keyframes规则

​	规定动画的时长

​	规定动画的名称

```css
div{
    width: 100px;
    height: 100px;
    background-color: red;
    position: relative;
    animation: anim 5s; /*指定动画名称为anim执行时间为5s 执行次数为无限*/
    -webkit-animation: anim 0.4s infinite;
}
@keyframes  anim{
    0%{background-color: red;left: 0;top: 0}
    25%{background-color: blue;left: 200;top:0px}
    50%{background-color: coral;left: 200px;top: 200px}
    75%{background-color: cornflowerblue;left: 0px;top: 200px}
    100%{background-color: red;left: 0;top: 0px}
}
```

## 多列

1. 在CSS3中，可以创建多列来对文本或者区域来进行布局

2. 属性：

   column-count

   column-gap

   column-rule

## CSS瀑布流效果

```css
.container{
    column-width: 250px;            /*多列*/
    -webkit-column-width: 250px;
    -webkit-column-gap: 5px;            /*图片间距5px*/
}
.container div{
    width: 250px;               /*每张图片宽度为250px 高度自适应*/
    margin: 5px 0;
}
.container p{
    text-align: center;
}
```

