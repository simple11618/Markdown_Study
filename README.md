

参考： https://markdown-zh.readthedocs.io/en/latest/blockelements/

块级元素

段落和换行
	
	段落就是连续行上的文本，一个或多个空行划分不同的段落
	普通段落不应该使用缩进


	段落是由一个或多行连续文本组成，这条规则使得Markdown支持“硬换行”
	这个其他的文本到HTML转换器有很大不同，通常这些转换器会将段落中的
	每一个行都转换为一个<br />标签

	当你确定需要在Markdown中输入 <br />标签，只需要在行尾加上
	两个及以上的空格，然后换行


标题
	
	Markdown支持两种形式的标题，[Setext][1]和[atx][2]

	Setext样式的标题使用的等号来表示一级标题，使用连字符表示二级标题
	例如：

		This is an H1
		=============

		This is an H2
		-------------

		任意长度的=或-都是可以的


	Atx样式的标题每行开头使用1-6#号后跟个 空格 ，对应1-6级标题，例如：

		# This is an H1

		## This is an 

		##### This is an H5


块引用
	
	Markdown使用email样式的 > 字符作为块引用
	最好对引用文本才用强制换行并在 每一行行首加一个 > 后接一个空格

		> 这是引用测试
		> 第二行
		> 第三行


	Markdown中可以简单在每一个需要强制换行的段落的首行前面加一个 >

		> 引用哦
			这也是哦

		> 我也是引用的哦


	块引用可以嵌套，只需添加额外层级 > 即可

		> 一层引用

		>> 二层引用

		>>> 三层引用


	块引用可以包含Markdown元素，包括标题，列表和代码块

		> # 这是引用内容标题

		> 1.  啦啦啦
		> 2.  啦啦啦2


列表
	
	Markdown支持有序列表和无序列表

	无序列表使用星号，加号，和连字符 - 
	这些字符是可互换的，-为常用列表标记

		* 红
		* 黄
		* 蓝

		等价于

		+ 红
		+ 黄
		+ 蓝

		或

		- 红
		- 黄
		- 蓝

	有序列表使用数字加 点号

		1. 红
		2. 黄
		3. 蓝


	如果列表中包含空行，Markdown会在HTML输出中用<p>来包裹他们

		- 	红
		-	黄

		会输出

			<ul>
			<li>Bird</li>
			<li>Magic</li>
			</ul>

		但是

		-	红
		-	黄

		会输出
			
			<ul>
			<li><p>Bird</p></li>
			<li><p>Magic</p></li>
			</ul>	

	
	列表项可能包含多个段落，列表项中每个段落都必须用
	4个空格或 一个水平制表符来缩进

		1.    段落1
			  段落2
			  段落3

		2. 	  段落1
			  段落2
			  堕落3


		悬挂缩进只是为了更美观，而非强制要求


	如果列表项中包含块注释，块注释标记 > 需要缩进

		*  这是一个块注释

			> 这是注释
			> 注释哦


	如果列表项中有代码块，代码块需要 双倍缩进 
	用8个空格或两个水平制表符

		*	这是代码块
				<代码内容>


代码块
	
	预格式化的代码块用于输出编程语言和标记语言
	不同于普通段落，代码块中的行会被原样呈现

	Markdown会用 <pre> 和 <code> 标签包围代码块


	要在Markdown中插入代码块，只需要将每一行都缩进4个空格
	或1个水平制表符

		这是常规行
			这是一个代码行

	markdown会生成

		<p>这是常规行</p>
		<pre><code>这是一个代码行</code></pre>


	只有一级缩进，4个空格或1个水平制表符
	会从代码中的每一行中移除
	
	代码块自动扩展直到碰到未使用缩进的文本


	在代码块内，& 和 < > 或自动转换为HTML字符实体
	这是的Markdown包含HTML代码非常容易
	只需粘贴并缩进，Markdown会自动转换字符实体

	Markdown的语法在代码块中是无效的，例如
	代码块中的星号只是它的字面量而已，这是的用Markdown
	来书写Markdown自身的语法很容易



水平线
	
	一行中只要有3个以上的连字符，星号，或者下划线则会在该位置
	生成一个<hr />标签，星号和连字符之间的空格也是允许的

		***
		* * * *
		------
		=========






