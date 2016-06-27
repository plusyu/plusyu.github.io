---
layout: post
title: IOS 生命周期
categories: [ios]
tags: [ios]
description: ios 生命周期
---

从A跳转到B执行的顺序是：
B viewDidLoad ------> A viewWillDisappear -------> B viewWillAppear ------->B viewDidAppear ----- A viewDidDisappear

从B返回A执行的顺序是

 B viewWillDisappear------->A  viewWillAppear-------->A  viewDidAppear------>B viewDidDisappear



1、initWithCoder 或者 initWithNibName:Bundle  代码 nil
2、awakeFromNib
3、loadView
4、viewDidLoad
5、viewWillAppear
6、viewWillLayoutSubviews  子视图位置布局
7、viewDidLayoutSubviews
8、viewDidAppear
9、viewWillDisappear
10、viewDidDisappear
