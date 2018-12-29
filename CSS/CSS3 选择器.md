# CSS3 选择器

## 1. 元素选择器

最常见的选择器就是元素选择器，文档的元素就是最基本的选择器

例如：`h1{} a{}  `

## 2. 选择器分组

1. 例子

   ```css
   h1,h2{
       
   }
   ```

2. 通配符

   ```css
   *{
       margin: 0px;
   }
   ```

   给html文档中没有特意设定样式的标签一个默认的样式，如果后面向要对某个标签的样式进行定义，直接写可以覆盖通配符的样式。

## 3. 类选择器

* 类选择器允许以一种独立于文档的方式来指定样式

​	`.class{}`

* 结合元素选择器：

  例如： `a.class{}`

* 多类选择器

  对多个类选择器使用相同的样式

  `.class.class{}`

  ```html
  <p class="p1">this is my page</p>
  <p class="p2">this is my page</p>
  <p class="p1 p2">this is my page</p>
  ```

  ```css
  .p1{
      font-size: large;
  }
  .p2{
      color: blue;
  }
  .p1.p2{
      font-style: italic
  }
  ```

  这样第三个标签`.p1.p2`既拥有了从p1和p2继承的样式，也拥有了自己定义的新样式。

## 4. id选择器

1. id选择器类似于类选择器，不过也有一些重要差别

   实例：`#id{}`

2. 类选择器和id选择器之间的差别

   * id只能在文档中使用一次，而类可以使用多次
   * id选择器不能结合使用
   * 当使用js的时候，需要用到id（js中的方法getElementById）

## 5. 属性选择器

1. 简单的 属性选择器：

   例如： `[title]{}`

2. 根据具体的属性值来进行选择

   除了选择拥有某些元素，还可以进一步缩小范围，只选择拥有特定属性值的元素

   例如： `a[href = "http://www.baidu.com"]{};`

3. 属性和属性值必须完全匹配

4. 根据部分属性值来进行选择（部分匹配）

   ```html
   [title~="title"]{
       font-size: 50px;
   }
   <p tile="tit">hello</p>
   <p tile="title">hello</p>
   <p tile="table">hello</p>
   <p tile="title table">hello</p>
   ```

   在这个样例当中，只有第一个和第三个的字体大小会发生改变，这是因为只有第一个和第三个p标签能和title进行部分匹配。

## 6. 后代选择器

后代选择器可以选择作为某元素后代(儿子、孙子、曾孙...）的元素

```html
<p>
    this is my <strong>web<i>hello</i></strong> page
</p>
```

```css
p strong{
    color: blue;
}
p i{
    font-size: large;
}
```

## 7. 子元素选择器

1. 与后代选择器相比，子元素选择器只能选择作为某元素子元素的元素

   例如：`h1>strong{}`

   ```css
   p>strong>i{
       font-size: large;
   }
   p>i{
       这样是无效的，但是在后代选择器那里可以。
   }
   ```

## 8. 相邻兄弟选择器（应用不多）

可以选择紧接在另一个元素后的元素，且二者有相同的父元素

例如：`h1+p{};`

```html
<div>
    <ul>
        <li>item1</li>
        <li>item1</li>
        <li>item1</li>
    </ul>
</div>
```

```css
li+li{
    font-size: 50px;
}
```

这里只有后面两个li标签有效果

