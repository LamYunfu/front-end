# HTML5和HTML4的区别

## 推出的理由及目标

意图是将目前web上存在的各种问题一并解决掉，问题包括：

* Web浏览器之间的 兼容性很低
* 文档结构不够明确
* Web应用程序的功能受到了限制

### 语法的改变

* 内容类型

* DOCTYPE声明

  html4需要明确地声明html的版本，但是在html5中这是不需要的

* 指定字符编码

  * html4

    ```html
    <meta http-equiv="content-type" content="text/html;charset=UTF-8">
    ```

  * html5

    ```html
    <meta charset="UTF-8">
    ```

* 可以省略标记的元素

* 具有boolean值的属性

  ```html
  <input type="checkbox" checked>
  <input type="checkbox" checked="checked">
  <input type="checkbox" checked="">
  <input type="checkbox">
  前面三个表示true,最后一个表示false
  ```

* 省略引号

  指定属性值的时候可以将引号省略

  ```html
  <input type=checkbox>
  ```

---

## 新增的元素和废除的元素

* 新增的结构元素

  section	article	aside	header	footer	nav	figure

* 新增的其它元素

  vedio	audio	embed	mark	progress	meter	time	ruby	rt	rp	wbr	

  canvas	command	details	datalist	datagrid		keygen	output	source	menu

* 新增的input元素的类型

  email	url	number		range	Date Pickers

废除的元素

* 能使用CSS替代的元素: basefont、big、center、font、s、tt、u等
* 不再使用frame框架
* 只有部分浏览器支持的元素
* 其它被废除的元素

---

## 新增的属性和废除的属性

新增的属性

* 表单相关的属性
* 链接相关的属性
* 其它属性

废除的属性

## 全局属性

可以对任何元素使用的属性

* contentEditable属性

  * 允许用户编辑元素内容，boolean类型值，指示元素是否可编辑

  ```html
  <h2>可编辑列表</h2>
  <ul contenteditable = "true"> <!---->
      <li>列表1</li>
      <li>列表2</li>
      <li>列表3</li>
  </ul>
  ```

  

* designMode属性

  * 用于指示整个页面是否可编辑，只能在js脚本内改变

* hidden属性

  * 通知浏览器不渲染该元素，该元素内容是不可见状态

  ```html
  <ul hidden="true"> <!---->
      <li>列表1</li>
      <li>列表2</li>
      <li>列表3</li>
  </ul>
  ```

  

* spellcheck属性

  * 对于用户输入的内容进行拼写和语法检查，常用于input输入框

* tabindex属性

  * 指定按`tab`键的访问次序，获取焦点

  ```html
  <a href="#" tabindex="1">hello</a>
  <a href="#" tabindex="3">hello</a>
  <a href="#" tabindex="2">hello</a>
  ```

  