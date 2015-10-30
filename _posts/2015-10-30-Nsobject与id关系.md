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

<h3>
什么是一个obejct?
</h3>

{% highlight ruby %}

/// Represents an instance of a class.
struct objc_object {
    Class isa  OBJC_ISA_AVAILABILITY;
};

{% endhighlight %}

<p>
object就是一个C Struct ，而这个Struct里面只有一个isa的指针，指向自己所属的类别。
</p>

<h3>
什么是Class
</h3>

{% highlight ruby %}

/// An opaque type that represents an Objective-C class.
typedef struct objc_class *Class;

{% endhighlight %}

<p>
Class本身也是一个C Struct.再看下objc_cass的定义
</p>








