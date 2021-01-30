---
layout: post
title: 'kali下配置go环境'
date: 2021-1-22
author: cccciri
color: rgb(255,210,32)
cover: 'http://on2171g4d.bkt.clouddn.com/jekyll-banner.png'
tags: kali linux go
---




### kali下配置go环境

https://studygolang.com/dl   下载Linux版本的安装包

在/usr/local下解压源码包

sudo tar -zxf go1.15.7.linux-amd64.tar.gz -C /usr/local

我安的版本是1.15.7

3、将 /usr/local/go/bin 目录添加至PATH环境变量

export PATH=$PATH:/usr/local/go/bin
我是在最下面添加的

4、测试环境

输入go version能看到版本号就表示安装成功了

5、建立工作空间

在/home目录下新建go目录（文件名随意），然后在go目录下分别新建三个目录：

src ---- 里面每一个子目录，就是一个包。包内是Go的源码文件
pkg ---- 编译后生成的，包的目标文件
bin ---- 生成的可执行文件。

6、设置GOPATH环境变量

vi /etc/profile

然后加入下面这行:

export GOPATH=/home/go

保存后，执行以下命令，使环境变量立即生效:

source /etc/profile

需要注意的是必须要用root用户来完成

sudo passwd root

su root

我是一开始没有用root用户导致使环境变量生效的那一步之后，输入go version 会显示command not found

删除文件 rm -r

删除文件夹 rm

创建文件夹 mkdir

创建文件 touch

编译当前路径下的.go go install

windows：在项目中使用 go mod init 初始化一下会在项目中生成 go.mod文件，来控制版本,实际上Linux也得有这一步哈哈


<iframe type="text/html" width="100%" height="385" src="http://www.youtube.com/embed/gfmjMWjn-Xg" frameborder="0"></iframe>