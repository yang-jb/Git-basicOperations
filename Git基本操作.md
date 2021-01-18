# Git基本操作

##### # 专用名词：Workspace(工作区)、Index/Stage(暂存区)、Repository(本地仓库)、Remote(远程仓库)

-----

### 新建代码库

> 在当前目录新建一个Git代码库

###### $ 	git	init

> 新建一个目录，将其初始化为Git代码库

###### $	git	init	[project-name]

> 下载一个项目和它的整个代码历史

###### $	git	clone	[url]

--------

### 配置

> 显示当前的Git配置

###### $	git	config	-- list

> 编辑Git配置文件

###### $	git	config	-e	[--global]

> 设置提交代码时的用户信息

###### $	git	config	[--global]	user.name	"[name]"

###### $	git	config	[--global]	user.email	"[email	address]"

------

### 增加/删除文件

> 添加指定文件到暂存区

###### $	git	add	[file1]	[file2]

> 添加当前目录的所有文件到暂存区

###### $	git	add	.

> 删除工作区文件，并且将这次删除放入暂存区

###### $	git	rm	[file1]	[file2]

> 改名文件，并且将这个改名放入暂存区

###### $	git	mv	[file-original]	[file-renamed]

------

### 代码提交

> 提交暂存区到本地仓库

###### $	git	commit	-m	"提交的描述"

> 提交暂存区指定文件到仓库区

###### $	git	commit	[file]	-m	"提交的描述"

> 提交时显示所有diff信息

###### $	git	commit	-v

> 将add和commit合为一步

###### $	git	commit	-am	'message'

------

### 分支

> 列出本地所有分支

###### $	git	branch

> 列出远程所有分支

###### $	git	branch	-r

> 列出所有本地分支和远程分支

###### $	git	branch	-a

> 新建一个分支，但依然停留在当前分支

###### $	git	branch	[branch-name]

> 新建一个分支，并切换到该分支

###### $	git	checkout	-b	[branch]

> 新建一个分支，与指定的远程分支建立追踪关系

###### $	git	branch	--track	[branch]	[remote-branch]

> 切换到指定分支，并更新工作区

###### $	git	checkout	[branch-name]

> 切换到上一个分支

###### $	git	checkout	-

> 合并指定分支到当前分支

###### $	git	merge	[branch]

> 删除分支

###### $	git	branch	-d	[branch-name]

> 删除远程分支

###### $	git	push	origin	--delete	[branch-name]

###### $	git	branch	dr	[remote/branch]

> 检出版本v2.0

###### $	git	checkout	v2.0

-------

### 标签

> 列出所有tag

###### $	git	tag

> 新建一个分支tag在当前commit

###### $	git	tag	[tag]

> 新建一个tag在指定commit

###### $	git	tag	[tag]	[commit]

> 删除本地tag

###### $	git	tag	-d	[tag]

> 查看tag信息

###### $	git	show	[tag]

> 提交指定tag

###### $	git	push	[remote]	[tag]

> 提交所有tag

###### $	git	push	[remote]	--tags

-----

### 查看信息

> 显示有变更的文件

###### $	git	status

> 显示当前分支的版本历史

###### $	git	log

> 显示commit历史，以及每次commit发生变更的文件

###### $	git	log	--stat

> 显示指定文件相关的每一次diff

###### $	git	log	-p	[file]

> 显示过去五次提交

###### $	git	log	-5	--pretty	--oneline

> 显示暂存区和工作区的差异

###### $	git	diff

> 显示工作区与当前分支最新commit之间的差异

###### $	git	diff	HEAD

> 显示某次提交的元数据和内容变化

###### $	git	show	[commit]

-------

### 远程同步

> 下载远程仓库的所有变动

###### $	git	fetch	[remote]

> 显示所有远程仓库

###### $	git	remote	-v

> 显示某个远程仓库的信息

###### $	git	remote	show	[remote]

> 取回远程仓库的变化，并与本地分支合并

###### $	git	pull	[remote]	[branch]

> 上传本地指定分支到远程仓库

###### $	git	push	[remote]	[branch]

> 强行推送当前分支到远程仓库，即使有冲突

###### $	git	push	[remote]	--force

> 推送所有分支到远程仓库

###### $	git	push	[remote]	--all

--------

### 撤销

> 恢复暂存区的指定文件到工作区

###### $	git	checkout	[file]

> 恢复某个commit的指定文件到暂存区和工作区

###### $	git	checkout	[commit]	[file]

> 恢复暂存区的所有文件到工作区

###### $	git	checkout	.

> 重置暂存区与工作区，与上一次commit保持一致

###### $	git	reset	--hard

