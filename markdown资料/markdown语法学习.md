# markdown学习



[toc]

##  Typora入门博客

[Typora入门博客](https://www.cnblogs.com/hider/p/11614688.html#markdown%E4%BB%8B%E7%BB%8D)



## 1. 常用快捷键

![](C:\Users\wurun\AppData\Roaming\Typora\typora-user-images\image-20201016103145205.png)

### 	

### 1.1 一级标题至六级标题

一级标题至六级标题：`# `，`##`...（ctrl + 1,2,3...）

> # 一级标题
>
> ## 二级标题
>
> ### 三级标题
>
> #### 四级标题
>
> ##### 五级标题
>
> ###### 六级标题



### 	1.2 引用内容

引用内容：`> 内容`

> 引用内容
>
> 引用

### 	

### 	1.3 无序列表

使用 * + - 都可以创建一个无序列表 : `* ,+ ,- `

* aaa

* bbb

* ccc

  ### 1.4 有序序列

使用 1. 2. 3. 创建有序列表: `1. ,2. ,3. `

1. aa

2. bb

3. cc

   ## 1.5 任务列表

\ -[ ] 不勾选

\ -[x] 勾选 	

### 	1.6 代码块

两种方式：

1. 插入行内代码，使用反问号`(~键)、使用缩进

2. 插入多行代码输入3个反引号（```） + 回车，并在后面选择一个语言名称即可实现语法高亮。

   ```java
   def helloworld():
       print("hello, world!")
   ```



### 	1.7 数学表达式

​	插入数学表达式：按下$$，然后按下回车键，即可进行数学公式的编辑。

``` js
$$
\mathbf{V}_1\times\mathbf{V}_2 = \mathbf{X}_3
$$
```

结果如下：
$$
\mathbf{V}_1\times\mathbf{V}_2 = \mathbf{X}_3
$$


### 	1.8 插入表格

输入 `| 表头1 | 表头2 |`并回车。即可创建一个包含2列表。快捷键 `Ctrl + T`弹出对话框。

​	eg:`|id|number|`

| id   | number |
| ---- | ------ |
|      |        |

### 	1.9 分割线

输入 `***` 或者 `---` 再按回车即可绘制一条水平线，如下：
	1. 输入`***`，按下回车键

***

​	2. 输入`---`，按下回车键

---



### 	1.10 目录

输入 `[ toc ]` 然后回车，即可创建一个“目录”。TOC从文档中提取所有标题，其内容将自动更新。



## 2. markdown语法

### 	2.1 链接

这是一个带有标题属性的 `[链接1](http://example.com/ "标题")`
这是一个没有标题属性的 `[链接2](http://example.net/)`

[链接1](http://example.com/ "标题")

[链接2](http://example.net/)

### 	2.2 网址

网址链接：`<www.baidu.com>`

<www.baidu.com>

	### 	2.3 图片

图片链接形式：`![名称](url "标题")`

图片链接形式：`![名称](url)`

![Typora快捷键](C:\Users\wurun\AppData\Roaming\Typora\typora-user-images\image-20201016103145205.png)

### 	2.4 高亮

文本高亮语句：`==文本高亮==`	(需要设置)

### 	2.5 文本居中

文本居中语句：`<center>这是要居中的内容</center>`

<center>这是要居中的内容</center>

### 	2.6 转义

文本加粗：`**加粗的内容**`

=》**加粗的内容**

![转义](C:\Users\wurun\AppData\Roaming\Typora\typora-user-images\image-20201016105244937.png)