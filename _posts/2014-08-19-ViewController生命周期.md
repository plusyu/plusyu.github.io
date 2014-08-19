---
layout: post
title: IOS 生命周期
categories: [ios]
tags: [ios]
description: ios 生命周期
---

从A跳转到B执行的顺序是：
MainController  viewWillAppear------->MainController viewDidAppear---------->MainController  viewWillDisappear------->ServerController  viewWillAppear
------>MainController  viewDidDisappear--------->ServerController  viewDidAppear

从B返回A执行的顺序是

ServerController  viewWillDisappear------->MainController  viewWillAppear-------->ServerController  viewDidDisappear------>MainController viewDidAppear

