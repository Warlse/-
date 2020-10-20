# git常用命令

[toc]

## 1.专用名词

​	workspace:	工作区
​	Index/stage:	暂存区s
​	Repository:		仓库区（或本地仓库）
​	Remote:		远程仓库
​	

## 2.新建代码库

​	#在当前目录下新建一个Git代码库
​		$ git init
​		

	#新建一个目录，将其初始化为Git代码库
		$ git init [project-name]
		
	#下载一个项目和它的整个代码历史
		$ git clone [url]
		$ git clone git@github.com:Warlse/gitskill.com



## 3.配置

#显示当前的git配置
	$ git config --list

#设置提交代码时的用户信息
	$ git config [--global] user.name "Warlse"
	$ git config [--global] user.email "wurun20@163.com"



## 4.增加/删除文件

​	#添加文件到暂存区
​		$ git add [文件名]
​	

	#删除暂存区文件
		$ git rm --cache [文件名]
	
	#添加指定目录到暂存区，包括子目录
		$ git add [dir]
		
	#添加当前目录下的所有文件到暂存区
		$ git add .
	
	#删除工作区文件，并将这次删除放入暂存区
		$ git rm [文件名1] [文件名2]
		
	#改名文件，并将这个改名放入暂存区
		$ git mv [file-origin] [file-newName]



## 5.代码提交及关联远程仓库

​	#提交暂存区到仓库区
​		$ git commit -m "备注"
​		

	#提交暂存区的指定文件到仓库区
		$ git commit [文件名1] [文件名2] -m "备注"
		
	#提交工作区自上次commit之后的变化，直接到仓库区
		$ git commit -a
	
	#提交时显示所有diff信息
		$ git commit -v
		
	#关联远程仓库(origin:远程库的默认叫法)
		$ git remote add origin git@github.com:Warlse/learn.git 
		
	#推送本地库到远程库
		$ git push -u origin master(首次推送)
		$ git push origin master (非首次推送)



## 6.分支

​	#查看所有本地分支
​		$ git branch
​	

	#创建分支
		$ git branch [分支名]
		
	#切换分支
		$ git switch [分支名] 或 git checkout [分支名]
	
	#创建+切换分支
		$ git switch -c [分支名] 或
		$ git checkout -b [分支名]
		
	#合并分支到当前分支
		$ git merge [分支名]
	
	#删除分支
		$ git branch -d [分支名]



## 7.分治策略

​	#使用--no-ff参数，可进行普通模式合并
​	$ git merge --no-ff -m "[备注]" [分支名]
​	eg:$ git merge --no-ff -m "合并分支" dev
​	
​	

## 8. 远程克隆

### 更换git源加速

比如我们需要克隆github上**xx**的一项目**yy**。原来我们需要输入:

```php
git clone https://github.com/xx/yy
```

因为克隆站的地址为`https://github.com.cnpmjs.org`
 所以现在我们只需要输入:

```php
git clone https://github.com.cnpmjs.org/xx/yy
```



## 9、将新分支推送到github

命令如下：

```
git push origin [branch name]
```

例如：

```
git push origin gh-dev
```



## 10、删除本地分支

命令如下：

```
git branch -d [branch name]
```

例如：

```
git branch -d gh-dev
```



## 11、删除github远程分支

命令如下：

```
git push origin :[branch name]
```

分支名前的冒号代表删除。
例如：

```
git push origin :gh-dev
```



## 12、提交本地代码到新分支

### (1) 切换到新的分支

命令如下：

```
git checkout [branch name]
```

例如：

```
$ git checkout gh-dev
Switched to branch 'gh-dev'
```

### (2) 添加本地需要提交代码

命令如下：

```
git add .
```

### (3) 提交本地代码

命令如下：

```
git commit -m "add my code to new branchB"
```

### (4) push 到git仓库

命令如下：

```
git push origin [branch name]
```

例如：

```
git push origin gh-dev
```