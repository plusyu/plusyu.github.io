---
layout: post
title: RxSwift Flow
categories: [RxSwift]
tags: [RxSwift Flow]
description: RxSwift Flow
---

<h3>RxSwift 实现流程</h3>

<img src="{{ site.BASE_PATH }}/assets/ico/rxswiftflow.png" height="600" width="100%" class="img-rounded author-image" />

{% highlight ruby %}

Observable.just("3")
            .map{$0 + "map"}
            .subscribe { event in
                print(event)
        }

{% endhighlight %}

<p>根据上面的类图，可以分为两大类。</p>
<p>1、Obserable（被监听者）</p>
<p>2、Observer（监听者）</p>















<p>参考</p>
<p>http://triplecc.github.io/blog/2016-10-01-rxswiftshi-xian-chu-tan/ </p>