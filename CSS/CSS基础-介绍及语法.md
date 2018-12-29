# CSS基础-介绍及语法

## CSS介绍

1.CSS概述：

​	CSS指层叠样式表

​	CSS样式表极大地提高了工作效率

###CSS基础语法

```css
selector{
    property: value
}
```

例：`h1:{color:red;font-size:14px;}`

属性大于一个之后，属性之间用分号隔开

如果值大于一个单词，则需要加上引号：

```css
p{
    font-family:"sans serif";
}
```

### CSS高级语法

1. 选择器分组

   ```css
   h1,h2,h3,h4,h5,h6{
       color:red;
   }
   ```

2. 继承

   未被引入样式的标签会继承上级标签的样式。

```css
body{
    color:blue;
}
```

---

## CSS派生选择器

1. 派生选择器

   通过依据元素在其位置的上下文关系来定义样式

   ```css
   li strong{
       color: red;
   }
   
   <li><strong>li标签：Hello</strong></li>
   ```


### CSSid选择器

1. id选择器

   id选择器可以为标有id的HTML元素指定特定的样式

   id选择器以“#”来定义

```css
<p id="pid">hello css</p>
#pid{
    color: yellow;
}
```

2. id选择器和派生选择器

   目前比较常用的方式是id选择器常常用于建立派生选择器

```css
<p id="pid">hello css<a href="http://www.baidu">百度</a></p>
#pid a{
     color: yellow;
}
```

---

## CSS类选择器

1. 类选择器

   类选择器以一个点显示

   ```css
   .pclasss{
       color: aqua;
   }
   <p class="pclasss">hello css</p>
   ```

2. class也可以用作派生选择器

   ```css
   .pclasss a{
       color: aqua;
   }
   <p class="pclasss">hello css<a>蓝云甫</a></p>
   ```

---

## CSS属性选择器

1. 属性选择器：

   对带有指定属性的HTML元素设置样式

2. 属性和值选择器

```css
<style type="text/css">
        [title]{          //属性选择器没有指定具体的值，值任意
            color: blue;
        }
        [title=te]{		//属性选择器指定具体的值，必须是该值的属性才能渲染
            color: coral;
        }
 </style>

 <p title="t">属性选择器</p>
 <p title="te">属性选择器</p>
```

