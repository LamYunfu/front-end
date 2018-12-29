# HTML框架、背景和实体

## HTML框架

1. 框架标签（frame）:

​	框架对于页面设计有很大的 作用

2. 框架集标签（<frameset>）

   框架集标签定义如何将窗口分割为框架

   每一个frameset定义一系列行或列

   rows/cols的值规定了每行或每列占据屏幕的面积

3. 常用标签

   noresize: 固定框架的大小

   cols: 列

   rows: 行

4. 内联框架(HTML5仍然在使用)

   iframe

   ```html
   <body bgcolor="#ff7f50">
       FrameC
       <br/>
       <iframe src="frameB.html" width="600" height="600"></iframe>
   </body>
   ```

   

---

## HTML背景

1. 背景标签

   Background

2. 背景颜色

   Bgcolor

   ```html
   <body background="Holding%20On_109951163068069545.jpg">
   ```

3. 颜色：

   * 颜色是由一个十六进制符号来定义，这个符号由红绿蓝三种颜色的值组成（RGB）
   * 颜色最小值：0(#00)
   * 颜色最大值255(#FF)
     * 红色：#FF0000
     * 绿色：#00FF00
     * 蓝色：#0000FF
   * 具体的命名代号：black、coral

   ---

   ## HTML实体（转义字符）

   1. 实体：

      HTML中预留字符串必须被替换成字符实体

      如：<、>、&

   