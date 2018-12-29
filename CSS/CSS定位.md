# CSS定位

改变元素在页面中的位置

1. CSS定位机制：
   * 普通流：元素按照其在HTML中的位置顺序决定排布的 过程
   * 浮动
   * 绝对布局
2. CSS定位属性：

| 属性           | 描述                                                 |
| -------------- | ---------------------------------------------------- |
| positon        | 把元素放在一个静态的、相对的、绝对的、或固定的位置上 |
| top            | 元素向上的偏移量                                     |
| left           | 元素向左偏移量                                       |
| right          | 元素向右偏移量                                       |
| bottom         | 元素向下的偏移量                                     |
| overflow       | 设置元素溢出其区域发生的事情                         |
| clip           | 设置元素显示的形状                                   |
| vertical-align | 设置元素垂直的对齐方式                               |
| z-index        | 设置元素的堆叠顺序                                   |

3. CSS position属性
   * static           		静态位置
   * relative                   相对其它元素的位置
   * absolute                  绝对位置
   * fixed                         固定位置（不随页面滚动而变化）

```css
#position1{
    width: 100px;
    height: 100px;
    background-color: bisque;
    position: relative;
    left: 10px;
    top: 20px;
    z-index: 2;         /*谁的大，谁呈现在前面*/
}
```



## CSS浮动

1. 浮动float属性可用值：
   * left:元素向左浮动
   * right：元素向右浮动
   * none:元素不浮动
   * inherit:从父级继承浮动属性

```css
#fd{
    width: 100px;
    height: 150px;
    background-color: chartreuse;
    float: left;            /*从页面中抠出来进行浮动*/
}
```

1. clear属性：

   去掉浮动属性（包括继承来的属性）

   clear属性可用值：

   * left、right: 去掉元素向左右浮动
   * both:两侧均去掉浮动
   * inherit: 去掉从父级继承而来的浮动属性

   ```css
   .text{
       clear:left;             /*去掉向左浮动的一个效果*/
   }
   ```

   ### CSS浮动的应用
