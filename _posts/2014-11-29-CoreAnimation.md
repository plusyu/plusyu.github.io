---
layout: post
title: Core Animation
categories: [ios]
tags: [ios]
description: Core Animation
---

{% highlight ruby %}

-(CGRect) frame  
{  
     float x = center.x - layer.anchorPoint.x * bounds.width;   
     float y = center.y - layer.anchorPoint.y * bounds.height;  
     float width = bounds.width;
     float height = bounds.height;  
     return CGRectMake(x, y, width, height);
}

{% endhighlight %}

{% highlight ruby %}

-(void) setFrame:(CGRect) rect
{
    center.x = rect.x + layer.anchorPoint.x * rect.width;
    center.y = rect.y + layer.anchorPoint.y * rect.height;
    bounds.width = rect.width;
    bounds.height = rect.height;
}

{% endhighlight %}

任何时候：
layer.position === center



bounds.x和bounds.y只控制aView下所有subView的原点坐标。

图层的 position 属性是一个 CGPoint 的值，它指定图层相当于它父图层的位置,该值基于父图层的坐标系。

图层的 bounds 属性是一个 CGRect 的值，指定图层的大小(bounds.size)和图层的原点(bounds.origin)。

图层的 anchorPoint 属性是一个 CGPoint 值，它指定了一个基于图层 bounds 的符合位置坐标系的位置。

锚点（anchor point）指定了 bounds 相对于 position 的值，同时也作为变换时候的支点。

锚点使用单元空间坐标系表示，（0.0，0.0）点接近图层的原点，而（1.0，1.0）是原点的对角点。改变图层的父图层

的变换属性（如果存在的话）将会影响到 anchorPoint 的方向，具体变化取决于父图层坐标系的 Y 轴。

当你设置图层的 frame 属性的时候，position 会根据锚点（anchorPoint）相应的改变，而当你设置图层的

position 属性的时候，bounds 会根据锚点(anchorPoint)做相应的改变。

默认anchorPoint:(0.5,0.5)

改变anchorPoint的时候,center不会改变。frame会随着发生改变









