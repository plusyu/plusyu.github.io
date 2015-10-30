---
layout: post
title: NSObject
categories: [ios]
tags: [ios]
description: NSObject id
---

<h3>什么是id</h3>

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

{% highlight ruby %}

struct objc_class {
    Class isa  OBJC_ISA_AVAILABILITY;

#if !__OBJC2__
    Class super_class                                        OBJC2_UNAVAILABLE;
    const char *name                                         OBJC2_UNAVAILABLE;
    long version                                             OBJC2_UNAVAILABLE;
    long info                                                OBJC2_UNAVAILABLE;
    long instance_size                                       OBJC2_UNAVAILABLE;
    struct objc_ivar_list *ivars                             OBJC2_UNAVAILABLE;
    struct objc_method_list **methodLists                    OBJC2_UNAVAILABLE;
    struct objc_cache *cache                                 OBJC2_UNAVAILABLE;
    struct objc_protocol_list *protocols                     OBJC2_UNAVAILABLE;
#endif

} OBJC2_UNAVAILABLE;

{% endhighlight %}

<p>
类型也是一个C Struct ，最开始的那个isa指向它的所属类别。
super_class则指向这的父类别。  
</p>

<h3>什么是Meta Class</h3>
<p>
1、每个Class（NSObject）的isa指针都指向唯一的Class，这个Class称之为Meta Class
</p>
<p>
2、每个Meta Class的isa指针都是指向最上层的Meta Class，最上层的Meta Class的isa则是指向自己，形成回路
</p>
<p>
3、每个meta class的super_class指针都是指向它原本类别的super class的meta class,但最上层的Meta Class的super_class则是指向NSObject类别本身。
</p>
<p>
4、最上层的Class(NSObject),它的Super Class指向nil.
</p>

 <img src="{{ site.BASE_PATH }}/assets/ico/objective-c-object-model.png" height="524"  class="img-rounded author-image" />


<h3>
	什么是instancetype?
</h3>

<p>
“instancetype is a contextual keyword that is only permitted in the result type of an Objective-C method”
</p>
instancetype就只是一个关键字，它告诉编译器回传类型，让编译器可以在编译阶段就有足够的信息来判断程序是否有问题。
<p>
<p>
instancetype 主要目的是为了帮助编译器更了解你的代码，在编程阶段发现问题
</p>
	


</p>


