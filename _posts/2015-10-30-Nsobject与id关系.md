---
layout: post
title: NSObject
categories: [ios]
tags: [ios]
description: NSObject id
---

1、什么是id

在objc.h中定义如下
{% highlight ruby %}

/// A pointer to an instance of a class.
typedef struct objc_object *id;

{% endhighlight %}

<p>
所谓的id就是一个指向实例(instance)的指针。id这个Struct的定义本身带一个*，这就是为什么在写其他实例时候需要加*，而写id不需要加*的原因。
</p>






