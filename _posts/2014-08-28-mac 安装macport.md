---
layout: post
title: macport安装javahl
categories: [ios]
tags: [ios]
description: ios 生命周期
---

在MAC OSX 下为了安装subclipse，安装完成后，总是提示找不到JavaHL,一通google后，说安装maport可以解决

1、安装subclipse
http://subclipse.tigris.org/update_1.8.x

2、安装macports
http://www.macports.org/
安装完成macports后，如果执行sudo port install xxx出现Port install not found错误，执行如下命令：
sudo port -v selfupdate
3、安装javahl
sudo port install subversion-javahlbindings

等待N久后，安装失败。


然后放弃这玩意。
安装javahl，其实只要在安装subclipse的时候，勾选SVNKit就可以了。无言。。。。。。。。。。。。。。。。。。。。。。。。。


git add .  
git commit -m 'init'
git push origin