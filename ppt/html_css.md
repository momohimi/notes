title: 入门系列之： HTML 和 CSS
speaker: 高静华
url: ''
transition: slide
files: /css/ppt.css

[slide]

# 入门系列之：**HTML** 和 **CSS**
### 遇到想问的请随时打断 

<div style="width: 100%; text-align: right">by GaoJinghua</div>


[slide]

#  HTML 和 CSS 是什么？


[slide]

## HTML

### 超文本标记语言（HyperText Mark-up Language）

* 超文本：图片、链接、音乐、程序等非文字元素 {:&.moveIn}
* 标语语言：不是一种编程语言，使用标记标签(markup tag)来描述网页

## CSS

### 级联样式表（Cascading Style Sheets）

* 定义如何显示HTML元素，解决内容与表现分离的问题 {:&.moveIn}
* 多重样式将层叠为一个

----

[slide]

# 它们在哪执行？从哪来？

[slide]

* ## 在浏览器中运行 {:&.fadeIn}
	* PC：IE系列，Chrome，Safari，国内各种套壳多核浏览器等 
	* 移动：Android 系统浏览器，Chrome，Safari等

* ## 存放于服务器，每次访问都需要获取
	* http 或 https 
	* 动态和静态

* ## 内嵌浏览器内核的APP
	* webview 
	* hybird app

----

[slide]

# 版本？

[slide]

## HTML5 和 HTML(4)
	* HTML5 是 HTML的第五次重大修改，2014年10月28日正式推出
	* 现代浏览器基本支持（Chrome, IE10+, Safari, FireFox）
	* 具体可见：<a href="http://www.w3.org/TR/HTML/" target="_blank">http://www.w3.org/TR/HTML/</a>

----

## CSS3 和 CSS(2.1)
	* 同样的，CSS3是CSS的升级版本，处于草案阶段
	* 现代浏览器基本支持
	* css4处于设计中
	* 具体可见：<a href="http://www.w3.org/TR/CSS/" target="_blank">http://www.w3.org/TR/CSS/</a>

[slide]

# 如何使用HTML？

[slide]

## 基本结构	
```html
<!DOCTYPE html>
<html>
	<head><title>网页标题</title></head>
	<body>
		欢迎加入PP租车！
	</body>
</html>
```
<iframe data-src="/ex/base.html" src="about:blank;" style="height: 60px;"></iframe>

----
* 浏览器不会显示HTML标签，只使用标签来解释页面内容 {:&.fadeIn}
* ```<!DOCTYPE html>``` 声明帮助浏览器正确地显示网页
* ```<html>```元素定义了整个文档
* ```<head>```元素用于指示浏览器获取网页信息
* ```<body>```元素定义了文档的主体，对用户可见

[slide]

* ## HTML片断 {:&.fadeIn}
```html
<div id="panda">
	<span class="fat" data-src="pathtoname">fat</span><br/>
	<input type="checkbox" value="20" checked>
</div>
```

* ## 元素 
	* 元素是指从开始标签到结束标签的所有代码
	* 元素可以嵌套，必须闭合
	* 不同元素有不同的适用场景

* ## 属性
	* 属性提供了关于HTML元素的更多信息
	* 属性通常以key-value对的形式出现，如id="panda"
	* 某些元素具有特有属性，属性可以自定义

----

[slide]

* ## 行内元素和块级元素 

	* **行内元素在同一行展示** {:&.fadeIn}

	```html
	<span>第一个</span><span>第二个</span>
	```
	> <span>第一个</span><span>第二个</span>

	* **块级元素独占一行**

	```html
	<div>第一个</div><div>第二个</div>
	```
	> <span>第一个</span><br><span>第二个</span>

	* **可以改变** 
	```html
	<span style="display: block">第一个</span><span>第二个</span>
	```
	> <span style="display: block">第一个</span><span>第二个</span>

----

[slide]

# 一些常用的HTML元素

----

[slide]

* ## 图片 ```<img>```

	* 语法
	```html
	<img src="path\to\img" alt="图片加载失败时显示这段文字" />
	```

	* 说明
		* src属性指定图片的位置，可以是绝对路径或相对路径
		* 若src属性为空，某些浏览器（IE）会自动加载当前页面，因此需避免出现这种情况
		* ```<img>```为行内元素
	
----

[slide]

* ## 表格 ```<table>```

	* 语法
	```html
	<table>
		<tr>
			<th>环境</th><th>扩展名</th><th>特点</th>
		</tr>
		<tr>
			<td>Less</td><td>js/nodejs</td><td>.less</td><td>老牌，支持js解析</td>
		</tr>
		<tr>
			<td>Sass</td><td>Ruby</td><td>.scss/.sass</td><td>功能全，有成型框架，发展快</td>
		</tr>
	</table>

	```

	* 效果
	<table style="font-size: 12px;">
		<tr>
			<th></th><th>环境</th><th>扩展名</th><th>特点</th><th>案例</th>
		</tr>
		<tr>
			<td>Less</td><td>js/nodejs</td><td>.less</td><td>老牌，支持js解析</td><td>Bootstrap</td>
		</tr>
		<tr>
			<td>Sass</td><td>Ruby</td><td>.scss/.sass</td><td>功能全，有成型框架，发展快</td><td>Compass Bootstrap</td>
		</tr>
	</table>

----

[slide]

* ## 表格 ```<table>```

	* 说明
		* 简单的 HTML 表格由 table 元素以及一个或多个 tr、th 或 td 元素组成
		* tr 元素定义表格行，th 元素定义表头，td 元素定义表格单元
		* ```<table>```为块级元素

----

[slide]

* ## 表单 ```<form>```

	* 用于为用户创建输入，并向服务器传输数据

	* 语法
	```html
	<form action="/path/to/submit" method="POST">
	 	<p>姓名: <input type="text" name="name" /></p>
	 	<p>年龄: <input type="text" name="age" /></p>
	 	<input type="submit" value="提交" />
	</form>
	```
	
	* 效果
	<form action="/path/to/submit" method="POST" style="border: 1px dashed #fff; margin: 8px; font-size: 12px;">
	 	<p style="margin: 8px; ">姓名: <input type="text" name="name" /></p>
	 	<p style="margin: 8px; ">年龄: <input type="text" name="age" /></p>
	 	<p  style="margin: 8px; "><input type="submit" value="提交" /></p>
	</form>

----

[slide]

* ## 表单 ```<form>```

	* 说明
		* action属性规定当提交表单时向何处发送表单数据
		* method属性规定用于提交表单的http方法，只能是get或post，大小写不敏感
		* 表单能够包含 input 元素，比如文本字段、复选框、单选框、提交按钮等
		* 每个input元素的name属性定义提交字段名称
		* 当input元素的type为submit时，此按钮为提交按钮，点击可触发表单提交
		* ```<form>```为块级元素

----

[slide]

# 如何改变HTML元素的外观 ？

[slide]

* ## 浏览器缺省设置 {:&.fadeIn}
	* 不可修改
	* 随浏览器&操作系统的不同而不同

* ## 内联样式（元素的style属性） 

	```html
	<span>默认的字</span><span style="color:red">红色的字</span>
	```
	> <span>默认的字</span><span style="color:red">红色的字</span>

----

[slide]

# 那么，问题就来了：CSS呢？

[slide]

* ## CSS基础语法
	* CSS规则由两个主要部分构成：**选择器** 和 **一条或多条声明**
	* code：
	```css
	h1 {color:red; font-size:14px;}
	```
	* 一张图：<br>
	![ex](http://www.w3school.com.cn/i/ct_css_selector.gif 'info')

----

[slide]

* ## 选择器
	* 在CSS中，**选择器**是一种模式，**用于选择**需要添加样式的**HTML元素**
	* 注意大小写敏感
	* 常用的有：
		* ID选择器，如 #id
		* 类选择器，如 .class
		* 标签选择器，如 div
	* 更多请看：<a href="http://www.w3school.com.cn/cssref/css_selectors.asp" target="_blank">CSS 选择器参考手册</a>

----

[slide]

* ##内联样式表 

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title>网页标题</title>
		<style>
			div {font-family: 'Microsoft Yahei'; font-size: 24px;}
			.color {color: #f60;}
		</style>
	</head>
	<body>
		<div>
			欢迎加入<span class="color">PP租车！</span>
		</div>
	</body>
</html>
```
<iframe data-src="/ex/nocss.html" src="about:blank;" style="height: 100px;"></iframe>

----

[slide]

* ##外联样式表

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title>网页标题</title>
		<link rel="stylesheet" href="with.css">
	</head>
	<body>
		<div>
			欢迎加入<span class="color">PP租车！</span>
		</div>
	</body>
</html>
```
<iframe data-src="/ex/withcss.html" src="about:blank;" style="height: 200px;"></iframe>

----

[slide]

# 推荐阅读

[slide]

## 基本款

* <a href="http://item.jd.com/11457854.html" target="_blank">书籍：HTML5与CSS3基础教程</a>
* <a href="http://www.w3school.com.cn/h.asp" target="_blank">站点：W3School</a>

----

## 进阶款

* <a href="http://item.jd.com/11518108.html" target="_blank">书籍：响应式Web设计：HTML5和CSS3实践指南</a>
* <a href="http://item.jd.com/11535621.html" target="_blank">书籍：CSS高效开发实战：CSS 3、LESS、SASS、Bootstrap... </a>