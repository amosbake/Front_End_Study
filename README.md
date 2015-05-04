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
###html列表
1.	`<ol>`有序列表 type来指定列表顺序标识如 `a` `A``I``i` start指定开始时的标识
2.	`<ul>`无序列表 type来指定列表标识 `type="circle"`为空心圆 `disc`为实体圆 `square`为方块
3.	`<li>`列表项
4.	`<dl>`列表 自定义列表
5.	`<dt>`列表项 定义条件
6.	`<dd>`描述 定义描述
###html块
1.	块元素在显示时通常会以新行开始:如`<p>` `<h1>``<ul>`
2.	内联元素通常不会以新行开始如`<b>``<a>`
3.	`<div>` 通常配合样式使用
4.	`<span>`作为文本的容器
###html布局
1.	使用`<div>`布局 详见layout_div.html
2.	使用`<table>`布局 详见layout_tab.html
###html表单
input 包含了多种样式 用`type`指定 如:`text``password``checkbox``radio``button``summit`
`radio`实现单选效果要指定其分组`name=`
`select`实现下拉选择
`textarea`实现多行文本输入
详见form.html
###html实体
1.	html中预留字符串必须被替换成字符实体,如:<,>,&等
 	空格	`&nbsp;	&#160;`
<	小于号	`&lt;	&#60;`
>	大于号	`&gt;	&#62;`
&	和号	`&amp;	&#38;`
"	引号	`&quot;	&#34;`
'	撇号 	`&apos; (IE不支持)	&#39;`
￠	分`	&cent;	&#162;`
£	镑	`&pound;	&#163;`
¥	日圆	`&yen;	&#165;`
€	欧元	`&euro;	&#8364;`
§	小节`	&sect;	&#167;`
©	版权`	&copy;	&#169;`
®	注册商标	`&reg;	&#174;`
™	商标	`&trade;	&#8482;`
×	乘号	`&times;	&#215;`
÷	除号`	&divide;	&#247;`
##css 基础
###css概述
css是层叠样式表,定义了html的样式,方便了对html样式的操作
###css语法
基本语法如下
```
selector{
    property:value
}
```
派生选择器可以缩小指定范围
```
li strong{
    color: aqua;
    }
```
###id选择器
ID选择器以`#`定义,指定特定的样式,常用语建立派生选择器(`exp:demo.css`)
```
#id_2{
    color: chocolate;
    height: 300px;
    width: 300px;
    background-color: blanchedalmond;
}
```
###类选择器
类选择器以`.`定义,指定特定的样式,可以建立派生选择器(`exp:demo.css`)
```
.class_1{
    height: 300px;
    width: 300px;
    text-align: end;
}
```
###属性选择器
类选择器以`.`定义,指定特定的样式,可以建立派生选择器(`exp:demo_html`)
```
    <style type="text/css">
        [title]{
            color: blue;
        }
        [title=te]{
            color: red;
        }
    </style>
```
###CSS背景
example(`background.css`)
1.	`background-color`	规定要使用的背景颜色。
2.`	background-position`	规定背景图像的位置。
3.	`background-size`	规定背景图片的尺寸。
4.	`background-repeat	`规定如何重复背景图像。
5.	`background-origin`	规定背景图片的定位区域。
6.	`background-clip`	规定背景的绘制区域。
7.	`background-attachment	`规定背景图像是否固定或者随着 页面的其余部分滚动。
8.	`background-image`	规定要使用的背景图像。
###CSS文本
1.	`color	`设置文本的颜色。
2.	`direction	`规定文本的方向 / 书写方向。
3.	`letter-spacing	`设置字符间距。
4.	`line-height`	设置行高。
5.	`text-align`	规定文本的水平对齐方式。
5.	`text-decoration`	规定添加到文本的装饰效果。
6.	`text-indent`	规定文本块首行的缩进。
7.	`text-shadow`	规定添加到文本的阴影效果。
8.	`text-transform`	控制文本的大小写。
9.	`unicode-bidi`	设置文本方向。
10.	`white-space`	规定如何处理元素中的空白。
11.	`word-spacing`	设置单词间距。
12.	`hanging-punctuation`	规定标点字符是否位于线框之外。
13.	`punctuation-trim`	规定是否对标点字符进行修剪。
14.	`text-align-last	`设置如何对齐最后一行或紧挨着强制换行符之前的行。
15.	`text-emphasis	`向元素的文本应用重点标记以及重点标记的前景色。
16.	`text-justify`	规定当` text-align `设置为 "justify" 时所使用的对齐方法。
17.	`text-outline`	规定文本的轮廓。
18.	`text-overflow	`规定当文本溢出包含元素时发生的事情。
19.	`text-shadow`	向文本添加阴影。	css-3
20.	`text-wrap`	规定文本的换行规则。	css-3
21.	`word-break`	规定非中日韩文本的换行规则。
22.	`word-wrap`	允许对长的不可分割的单词进行分割并换行到下一行。
###CSS字体
1.	`	font	`在一个声明中设置所有字体属性。
2.	`font-family	`规定文本的字体系列。
3.	`	font-size	`规定文本的字体尺寸。
4.	`	font-size-adjust	`为元素规定 aspect 值。
5.	`font-stretch	`收缩或拉伸当前的字体系列。
6.	`font-style`	规定文本的字体样式。
7.	`font-variant`	规定是否以小型大写字母的字体显示文本。
8.	`font-weight	`规定字体的粗细。
##CSS对齐
1.  `margin` 居中
```
    margin-left: auto;
    margin-right: auto;
```
2.  `position`
```
    position: absolute;
    right: 0px;
```

3.  `float`
```
   float: left;
```
