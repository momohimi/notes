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

* ## 代码：

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

* ## JSON
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

* 语法
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

# DOM操作

[slide]

# 事件处理

[slide]

# AJAX

[slide]

# 推荐阅读