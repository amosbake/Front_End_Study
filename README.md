#前端开发学习笔记
##HTML 基础
###标签及常用属性(index.html)
1.	p标签代表单独一行的内容
2.	h表示标题 h1~h6表示标题字体的大小
3.	a定义一个超链接`<a href="http://www.163.com" target="_top">网易</a>`
4.	br/表示换行
5.	img表示一个图片`<img src="imgs\1341581055_3571.png"/>`
6.	title 表示网页的标题,显示在浏览器标签栏上的内容
7.	bgcolor 表示背景色  background表示背景图片
8.	align 表示对齐方式,默认是左对齐`<h1 align="right">标题h1</h1>`
9.	a标签的 target 表示在何处打开链接.
	-	`_blank` 打开新的标签页
	-	`_self`当前页面打开
	-	`_top` 框架
	-	`_parent`框架
10.	style的type属性来引用css样式
###html字体格式化(format.html)
```html
 <p>我是普通文字</p>
    我是<b>粗体</b>文字<br/>
    我是 <big>大号</big>文字--html_5 过时<br/>
    我是<em>斜体</em>文字<br/>
    我是<i>斜体</i>文字<br/>
    我是<small>小号</small>文字<br/>
    我是<strong>加重</strong>文字<br/>
    我是<sub>下标</sub>文字<br/>
    我是<sup>上标</sup>文字<br/>
    我是<ins>插入</ins>文字<br/>
    我是<del>删除</del>文字<br/>
```
###html样式(style.html)
1.	外部样式表:<br/>`<link rel="stylesheet" type="text/css" href="myStyle.css">`
2.	内部样式表:在头文件中指定<br/>`<style type="text/css">
        p{
            color: cornflowerblue;
        }`
3.	内联样式表:在标签内指定<br/>`<a href="https://www.baidu.com" style="color: darkgreen">点击我跳转到百度</a>`
###html链接(table.html)
1.	文本链接<br/> `<a href="https://www.baidu.com">点击我</a><br/>`
2.	图像链接<br/>` <a href="https://www.baidu.com"><img src="imgs\1341581055_3571.png"></a>`
3.	文档内的链接 跳转到name属性标识的地方<br/>`<a name="tips">hello</a><br/>
<a href="#tips">跳转到hello</a><br/>`
4.	设定宽高 alt属性表示图像不能显示时的替代文字<br/>` <a href="https://www.baidu.com"><img src="imgs\1341581055_3571.png" width="100px" height="100px"></a>`
###html表格
1.	`<table>`表格:<br/>
-	<b>`border="2px"`定义其边框</b> 
-	<b>单元格的内边距用 cellpadding设置</b> 
-	<b>单元格的间距用 cellspacing设置</b> 
2.	`<caption>`表格标题
3.	`<th>`表格表头:<br/> -	<b>表头也包含在`<tr>`中</b> 

4.	`<tr>`表格的行
5.	`<td>`表格单元:<br/> <b>表示空的单元格只需要不填写内容就行</b>
6.	`<thead>`表格的页眉
7.	`<tbody>`表格的主体
8.	`<tfoot>`表格的页脚
9.	`<col>`表格的列属性
