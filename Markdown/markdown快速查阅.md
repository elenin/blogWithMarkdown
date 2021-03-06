#Markdown语法简介
---
**快速学习Markdown，或者供Markdown书写者查阅**

---
##相关资源链接：

[Markdown语法介绍](http://wowubuntu.com/markdown/)

[轻量级标记语言介绍](http://www.worldhello.net/gotgithub/appendix/markups.html)

---
##目录

1. ###[区块元素](#blockElement)
2. ###[区段元素](#sectionElement)
3. ###[链接](#link)
4. ###[其他](#other)

---
<a name='blockElement'></a>
##区块元素

1. 段落

	Markdown的段落由一个空行来分割。
	就是说，如果没有使用空行，换行符将被忽略。
	另外，无法使用空格或者制表符来进行段落中的缩进。
	
2. 缩进
    
    &nbsp;&nbsp;缩进大概需要这样：
        
        &nbsp;&nbsp;缩进大概需要这样：

    `&nbsp;`在html中是空格转义之后的形式。
    记住，Markdown中支持html的语法，所以可以很方便(或者不得不)用html扩充。

3. 标题

    两种标题语法：
	
	1. 底线形式：
	
		任意数量的=代表最高阶标题
		
		任意数量的-代表第二阶标题
		
		例如：
			
			This is H1
			====
			This is H2
            --

    2. \#号形式：
	
		行首插入 1 到 6 个 # ，对应到标题 1 到 6 阶
		
		例如：
		
			# This is H1
			## This is H2
			###### This is H6
		
		可以选择是否闭合#号，不过只是纯装饰作用，不会影响最终解析的结果

4. 列表

	1. 有序列表
	
		使用数字点号空格的方式声明。
		
		例如：
		
			1. 第一
			2. 第二
			3. 第三
		
	2. 无序列表
		
		使用*或+，-三种符号作为列表标记。
		
		例如：
		
			* 嗯
			* 哼
			* 哈
			
		或者：
		
			+ 嗯
			+ 哼
			+ 哈
		
	**注意！**
	
		如果列表各项中插入别的Markdown区块元素，将会使列表顺序失效！
		**处理方法**：在区块元素(包括文本段落)前加四个空格或者制表符进行缩进。
		注意是在原来的基础上增加缩进。
		
5. 区块引用

	同电子邮件一样，使用>的方式。
	比如：
	
		> 先弄清楚事实，歪曲是之后的事。
		> 					—— 马克·吐温
	
	注意，在引用区块中可以使用其他Markdown语法。
	
	同理，如果要嵌套引用，就增加一个>
	
		> 让我们看看一个嵌套引用
		>
		>> 这是一个嵌套引用
		>
	
	 注意，如果在列表中使用引用，需要再增加缩进。
		
6. 代码区块

	加四个空格或者制表符进行缩进。
	就是这么简单。
	
	注意，如果在列表中使用引用，需要再增加缩进。
	
7. 分割线

	在一行中用三个以上的星号、减号、底线来建立一个分隔线，行内不能有其他东西。
	
	---

<a name="sectionElement"></a>
##区段元素

1. 强调

	使用`*`或`_`包围一段文本来生成`<em></em>`的效果。
	
	*斜体*
	
	使用`**`或`__`包围一段文本来生成`<strong></strong>`的效果。
	
	**加粗**
	
	如果你的 * 和 _ 两边都有空白的话，它们就只会被当成普通的符号。

2. 代码

	使用反引号把行内代码包起来。
	如果要在代码区段内插入反引号，你可以用多个反引号来开启和结束代码区段：
	
	`` 代码有反引号` ``
	
	代码区段的起始和结束端都可以放入一个空白，起始端后面一个，结束端前面一个，这样你就可以在区段的一开始就插入反引号：
	
	`` `反引号` ``
	
3. 图片

	图片链接语法分两种，行内式和参考式。
	
	行内式：
	
		![Alt text](/path/to/img.jpg)
	
	参考式：
	
		![Alt text][name]
		[name]: /path/to/img.jpg

<a name='link'></a>
##链接

1. 自动链接
	
	在网址和电子邮件地址包裹方括号，就可以生成链接。
	
	比如：
	
		<http://example.com/>
		<joe@example.com>
		
2. 生成链接

	Markdown生成的链接分两种，行内式和参考式。
	
	行内式把链接地址直接给到链接内容之后。
	参考式则在最后才给出链接的索引。
	
	比如：
	
		行内式：
		[github](https://github.com)
		或者加上title
		[github](https://github.com "github")
		
		支持相对路径：
		[here](/here/)
		
		参考式：
		[github][1]
		[1]: https://github.com "github"
		或者
		[github][]
		[github]: https://github.com "github"
	
	方括号括住的是生成链接的文本。
	
	同时注意，参考式里冒号之后必须留空白。
	而且最后面的title属性文本可以用双引号或括号包住。
	
<a name='other'></a>
##其他

<br />
可以使用\来对特殊符号进行转义。

可以在Markdown中嵌入html标记，正如这篇文章一样。
