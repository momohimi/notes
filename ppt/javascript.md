title: 入门系列之： Javascript
speaker: 高静华
url: ''
transition: slide
files: /css/ppt.css

[slide]

# 入门系列之：**Javascript**
### 遇到想问的请随时打断 

<div style="width: 100%; text-align: right">by GaoJinghua</div>


[slide]

# Javascript 是什么？


[slide]

* ## 描述：
	Javascript 是一种解释性脚本语言，它的解释器被称为Javascript引擎（浏览器的一部分）

* ## 组成部分：
	* **ECMAScript**，描述了语法和基本对象
	* 文档对象模型(**DOM**)，描述处理HTML内容的方法和接口
	* 浏览器对象模型(**BOM**)，描述与浏览器进行交互的方法和接口
	* 这三个部分，被浏览器不同程度的支持

* ## 基本用途：
	给HTML页面加添交互行为


[slide]

# 使用**&#60;script&#62;**标签插入Javascript


[slide]

* ## 内嵌 {:&.fadeIn}

	```html
	<script>
	function welcome() {
		//output welcome
	}
	</script>
	```

* ## 外联
	
	```html
	<script src="path/to/welcome.js"></script>

	```

* ## 位置
	可在页面任何位置插入```<script>```标签，但要记住```<script>```会阻塞页面渲染。

* ## 最佳实践
	尽可能在页面底部(```<body>```末尾)使用外联方式插入```<scipt>```

----

[slide]

# 基本概念（基于ECMA-262 第3版）

[slide]

* ## 代码：{:&.fadeIn}

	```script
	function welcome() {
		var words = 'welcome!';
		//output in console
		console.log(words);
	}
	welcome();
	```

* ## 说明：
	* Js语句以一个分号结尾；
	* 使用```var```关键字定义变量；
	* 单行注释使用```//```，多行注释使用```/* */```；
	* Js变量是弱类型，
	* 有5种基本数据类型：```Undefined、Null、Boolean、Number、String```
	
----

[slide]

# Object、Array、JSON

[slide]

* ## JSON {:&.fadeIn}
	JSON(Javascript Object Notation)，它是ECMA-262 第3版的一个子集，构建于两种结构：
	* “名称/值”对的集合，不同的语言中，它被理解为对象（object），结构（struct），哈希表（hash table），有键列表（keyed list），或者关联数组 （associative array）等。
	* 值的有序列表，在大部分语言中，被理解为数组(array)。

* ## Object
	```script	
	var obj = new Object(); //new 
	var obj = {}; //JSON
	```

* ## Array
	```script
	var arr = new Array();//new 
	var arr = []; //JSON
	```

[slide]

# Function

[slide]

* 语法 {:&.fadeIn}
	```script
	function functionName(arg0, arg1, ...., argN){
		//statements
		return result;
	}
	```

* 调用

	* ```functionName(arg0, arg1);```

* 返回值

	* 使用关键字```return```返回值

* 参数
	* Js函数没有签名概念：不要求传递参数的个数及其数据类型;
	* 参数在function内部用数组来表示，可通过arguments对象来访问；

----

[slide]

# 一些日常的JS使用
（基于jQuery）

[slide]
 
## DOM操作 

* ### 获取DOM元素 {:&.fadeIn}
 	* jQuery选择器语法：```var obj = $('selector')```
	* ID选择器：```var dom = $('#id')```
	* 类选择器：```var dom = $('.class')```
	* 标签选择器：```var dom = $('div')```
	* <a href="http://www.w3school.com.cn/jquery/jquery_ref_selectors.asp" target="_blank">jQuery选择器手册</a>
 
* ### 设置或获取DOM内容
	* 设置或返回所选元素的文本内容：```dom.text([value])```
	* 设置或返回所选元素的内容（包括 HTML 标记）：```dom.html([value])```
	* 设置或返回表单字段的值：```dom.val([value])```
 
* ### 设置或获取DOM属性
	```dom.attr([value])```

----

[slide]

## 事件

* 绑定事件 {:&.fadeIn}
	* 语法：```dom.on('eventName', function(event){})```
	* 说明
		* eventName：事件名称，如'click'
		* event: 事件对象，描述触发这次事件的具体信息

* 常用事件
	* 鼠标事件: 点击click, 悬停mouseover
	* 键盘事件：键盘按下keydown, 键盘弹起keyup
	* 焦点：获取焦点focus, 失去焦点blur

----

[slide]

## AJAX

* 代码
	```script
	$.ajax({
		type: 'GET/POST', //HTTP method
		url: 'path/to/target', //目标URL
		data: { key:value }, //数据
		dataType: 'json/html/text', //希望返回的数据类型
		success: function(result){}, //正常返回处理函数
		error: function(err){} //错误处理函数（超时，网络中断等）
	});
	```

----

[slide]

## 表单验证

* 外挂式：利用form的submit事件 {:&.fadeIn}
	* 代码：
	```script
	form.on('submit', function(event){
		//执行验证

		//如果验证不同过，通过return false阻止提交
		return false;
	});
	```

* 主动式：使用JS验证后提交表单
	* 代码：
	```script
	button.on('click', function(event){
		//执行验证

		//如果验证通过，提交表单
		form.submit();
	});
	```
----

[slide]

# 推荐阅读

[slide]

## 基本款

* <a href="http://item.jd.com/10951037.html" target="_blank">书籍：JavaScript高级程序设计（第3版）</a>
* <a href="http://item.jd.com/10960689.html" target="_blank">书籍：图灵程序设计丛书：jQuery实战（第2版）</a>

## 进阶款

* <a href="http://item.jd.com/10974436.html" target="_blank">书籍：JavaScript权威指南（第6版）</a>
* <a href="http://item.jd.com/11193885.html" target="_blank">书籍：编写可维护的JavaScript  </a>
* <a href="http://item.jd.com/11355978.html" target="_blank">书籍：深入浅出Node.js   </a>

----