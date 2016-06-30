---
layout: post
title: iOS  UIView
categories: [iOS]
tags: [iOS]
description: iOS UIView
---


<h5>layoutSubviews何时会被调用</h5>
<p>1、init初始化不会触发layoutSubviews</p>
<p>2、addSubview会触发layoutSubviews</p>
<p>3、设置view的Frame会触发layoutSubviews，当然前提是frame的值设置前后发生了变化</p>
<p>4、滚动一个UIScrollView会触发layoutSubviews</p>
<p>5、旋转Screen会触发父UIView上的layoutSubviews事件</p>
<p>6、改变一个UIView大小的时候也会触发父UIView上的layoutSubviews事件</p>
 
 





