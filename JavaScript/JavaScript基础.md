# JavaScript基础

## 1.介绍

* JavaScript是一种轻量级的编程语言
* JavaScript是可插入HTML页面的编程代码
* JavaScript插入HTML页面后，可由所有的浏览器执行

## 2.实现

* HTML中的脚本必须位于`<script></script>`标签之间
* 脚本可被放置在HTML页面的`<head>`和`<body>`部分中，通常放在`<head>`中，以不干扰页面内容。

## 3.输出

* JavaScript通常用来操作HTML

* 文档输出：

  ```js
  document.write("<p>this is my first JavaScript</p>");
  ```

## 4.语法

1. JavaScript语句：

   JavaScript语句向浏览器发出命令。语句的作用是告诉浏览器应该做什么。

2. 分号：

   语句之间的分割号是分号（;）

   分号是可选项，有时候是看不到以分号隔开的。

3. JavaScript代码:

   js代码是按照编写顺序来执行的

4. 标识符：

   JavaScript标识符必须以**字母、下划线或者美元符号**开始

   JavaScript关键字不可以被用作表示符。

5. JavaScript对大小写敏感

6. 空格：

   JavaScript会忽略掉多余的空格

7. 保留字

## 5. 注释

1. 单行注释： `//`
2. 多行注释：`/**/`
3. 快捷键：`ctrl + /`

## 6.变量和数据类型

### 变量

```javascript
var x = 10;
var y = 10.1;
var z = "Hello";
```

### 数据类型

1. 字符串(String)
2. 数字(Number)
3. 布尔(Boolean)
4. 数组(Array)
5. 对象(Object)
6. 空(null)
7. 未定义
8. 可以通过赋值为null的方式清除变量

```javascript
var string = "hello";
var i = 10;
var flag = true;
var arr = [1,2,3,4,5,6];
var arr = new Array("text", "text2", "text3");
var n = null;
var r;
r = 10;
r = null;
```



