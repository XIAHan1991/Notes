# 1.标题
## 类 atx 形式
如果一段文字被定义为标题，只要在这段文字前加 # 号即可.
总共六级标题，建议在井号后加一个空格。
可以在行尾加上 #，而行尾的 # 数量也不用和开头一样（行首的井字符数量决定标题的阶数）


	# title
	## title2
	### title3 ##


## 类 setext 形式
用底线的形式，利用 = （最高阶标题）和 - （第二阶标题）。
任何数量的 = 和 - 都可以有效果。


	This is an H1
	=============
	
	This is an H2
	-------------

tip:
>这里使用"---"时可能会与分割线造成困扰。要注意区分。可以通过空白行的使用来解决这个问题。


# 2.列表
列表的显示只需要在文字前加上 + 、- 或 * 即可变为无序列表。   
有序列表则直接在文字前加1. 2. 3. 符号要和文字之间加上一个字符的空格。

1. 如果要在列表项目内放进引用，那 > 就需要缩进；
2. 如果要放代码区块的话，该区块就需要缩进两次。
3. 在行首出现数字-句点-空白，要避免这样的状况，你可以在句点前面加上反斜杠。例如：  
	`1986. What a great season.`
可以写为  
	`1986\. What a great season.`  

```
1. 1st
2. 2nd
3. 3rd
```

1. 1st
2. 2nd
3. 3rd

```
- line1
+ line2
* line3
```

- line1
+ line2
* line3

# 3.引用
在文本前加入 > 这种尖括号（大于号）即可。  
1. 允许你偷懒只在整个段落的第一行最前面加上 >；  
2. 可以嵌套（例如：引用内的引用），只要根据层次加上不同数量的 >；  
3. 引用的区块内也可以使用其他的 Markdown 语法，包括标题、列表、代码区块等。

	>quote as an example
>quote as an example

# 4.链接与图片
链接为：`[]()`  
图片为：`![](){ImgCap}{/ImgCap}`  
## 链接 行内式
要建立一个行内式的链接，只要在方块括号后面紧接着圆括号并插入网址链接即可，如果你还想要加上链接的 title 文字，只要在网址后面，用双引号把 title 文字包起来即可。  

	This is [an example](http://example.com/ "Title") inline link.

This is [an example](http://example.com/ "Title") inline link.  

	[This link](http://example.net/) has no title attribute.

[This link](http://example.net/) has no title attribute.

## 链接 参考式
在链接文字的括号后面再接上另一个方括号，而在第二个方括号里面要填入用以辨识链接的标记。可以选择性地在两个方括号中间加上一个空格。接着，在文件的任意处，你可以把这个标记的链接内容定义出来。

>链接内容定义的形式为：  
- 方括号（前面可以选择性地加上**至多三个空格**来缩进），里面输入链接文字。辨别标签可以有字母、数字、空白和标点符号，但是并**不区分大小写**。**隐式链接标记功能**让你可以省略指定链接标记，这种情形下，链接标记会视为等同于链接文字，要用隐式链接标记只要在链接文字后面加上一个空的方括号;  
- 接着一个冒号;  
- 接着一个以上的空格或制表符;  
- 接着链接的网址，链接网址也可以用方括号包起来;  
- 选择性地接着 title 内容，可以用单引号、双引号或是括弧包着，可以把 title 属性放到下一行，也可以加一些缩进。   

>链接的定义可以放在文件中的任何一个地方，推荐直接放在链接出现段落的后面；把它放在文件最后面，就像是注解一样。


### exmple link
	I get 10 times more traffic from [Google] [1] than from[Yahoo] [2] or [MSN] [3].
	  [1]: http://google.com/        "Google"
	  [2]: http://search.yahoo.com/  "Yahoo Search"
	  [3]: http://search.msn.com/    "MSN Search"

I get 10 times more traffic from [Google] [1] than from
[Yahoo] [2] or [MSN] [3].
  [1]: http://google.com/        "Google"
  [2]: http://search.yahoo.com/  "Yahoo Search"
  [3]: http://search.msn.com/    "MSN Search"

## 图片
和链接很相似的语法来标记图片，同样也允许两种样式： 行内式和参考式。
### exmaple picture
	![example link](../Figures/github.png)
![example link](../Figures/github.png)

# 5.粗体、斜体、下划线
使用星号（*）和底线（_）作为标记强调字词的符号。  
用两个 * 包含一段文本就是粗体的语法，用一个 * 包含一段文本就是斜体的语法。

**粗体** `**粗体**`  
*斜体* `*斜体*`  
_下划线_ `_下划线_`  
==高亮== `==高亮==`  
~~删除线~~ `~~删除线~~`  
^上标 `^上标`

tips:
>1. 如果你的 * 和 _ 两边都有空白的话，它们就只会被当成普通的符号;
>2.	 如果要在文字前后直接插入普通的星号或底线，你可以用反斜线

# 6.表格
	| Tables        | Are           | Cool  |
	| ------------- |:-------------:| -----:|
	| col 3 is      | right-aligned | $1600 |
	| col 2 is      | centered      |   $12 |
	| zebra stripes | are neat      |    $1 |

| Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |


>作者：Te_Lee  
>链接：[http://www.jianshu.com/p/1e402922ee32/](http://www.jianshu.com/p/1e402922ee32/)

# 7.代码框
如果要标记一小段行内代码，你可以用反引号把它包起来（\`）。  
如果要在代码区段内插入反引号，你可以用多个反引号来开启和结束代码区段。  

	Use the `printf()` function.  
Use the `printf()` function.  

	``There is a literal backtick (`) here.``  
``There is a literal backtick (`) here.``  
# 8.代码区块
要在 Markdown 中建立代码区块很简单，只要简单地缩进 4 个空格或是 1 个制表符就可以。（代码块开始前需要有空行？？？）  

	example
	line1
		lien2
1. 这个每行一阶的缩进（4 个空格或是 1 个制表符），都会被移除；
2. 一个代码区块会一直持续到没有缩进的那一行（或是文件结尾）。  

# 9.分割线
在一行中用三个以上的星号、减号、底线来建立一个分隔线，行内不能有其他东西。你也可以在星号或是减号中间插入空格。

	* * *
	---
	___
	
example1:  `line with ***`.  
***
example2:  `line with ---`.  
- - -
example3:  `line with ___`.   
___


# 10.其他
支持以下这些符号前面加上反斜杠来帮助插入普通的符号。  

	\   反斜线
	`   反引号
	*   星号
	_   底线
	{}  花括号
	[]  方括号
	()  括弧
	#   井字号
	+   加号
	-   减号
	.   英文句点
	!   惊叹号
# END
>参考：[http://www.appinn.com/markdown/#precode](http://www.appinn.com/markdown/#precode)
