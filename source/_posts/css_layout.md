---
title: css之布局
date: {{ date }}
tags: [布局的技术手段, 响应式布局(设计), 固定布局(设计), 弹性布局(设计), 流动布局(设计), 媒体查询, flex]
categories: 
- css
series: css
---

我们都知道，定位、浮动、flexbox，这些可以用来布局；
我们也知道什么固定布局，流式布局等等，这些也是布局；
那么定位、浮动这些是什么布局呢，是固定布局吗?
都不是，所以固定布局、弹性布局、流式布局，这些更代表了一种布局的设计思想，一种布局方案，
而定位、浮动、flexbox这些是一种布局的技术手段。
我们大可这样理解：
布局的设计方式有 固定设计方式、弹性设计方式、流式设计方式、响应式设计方式;
布局的技术方法(手段)有 定位、浮动、flexbox、百分比；

## 布局的技术手段

### 优先使用flexbox，减少使用定位和浮动布局
布局的技术手段有：定位(绝对定位、固定定位)、浮动、flexbox。
在这些技术手段中，绝对定位、浮动这些已经是比较老的技术手段了，而且flexbox能够轻松实现浮动或绝对定位。
因为遇到布局时推荐优先使用新的布局方法 flexbox。

### display：gird
gird是最新的一种布局方式，可能在未来对目前的布局带来非常大的影响。

## 布局设计方式
### 布局方式介绍
参考《精通css》P177
**固定布局** 使用px布局；
**弹性布局** 使用em作为布局元素的尺寸。(不是用em来作为font-size或margin、padding哦)
**流式布局** 使用百分比布局，浏览器默认布局方式，也是主流布局方式。为什么说是主体布局方式了，因为响应式布局基本上基于流式布局。
**响应式布局** 基于流式布局，利用媒体查询等手段进行响应自适应，本质上响应式布局也是流式布局。《精通css》P207中，直接将响应式布局描述为：可以适配不同视口大小的流式布局。

有人说只要使用了em或者rem的就是一种弹性布局，这可能不太准确，笔记使用em来定义font-size或margin、padding等等是常识，使用rem来定义font-size等等，这些都是常识，可以说就是应该这样做的。所以如果使用rem或em做以上事情，就不应该是弹性布局。
只有使用em作为元素的宽高尺寸了，那才说明用了弹性布局。

### 响应式布局是当前最推荐方式
上面几种布局中，当有最推荐和最重要的是响应式布局，(又称为 响应式web布局设计)。

### 响应式布局
响应式布局主体用的还是流式布局，在此基础上，主要使用媒体查询进行响应设计，另外也使用了flexbox进行响应设计。
#### 媒体查询
自行网上查看。
#### flexbox
flexbox也是css中具有某种响应式特质的规范，无须使用媒体查询，flexbox本身就可以创建出能够有效利用空间的适配布局。
为什么说flexbox具备某种响应式特质呢，比如父级定义为flex，自己都会随着父级的变大而变大，缩小而缩小，这跟子级定义百分比，随父级增大而增大，缩小而缩小一样。说明了flexbox有浓烈的流式特性，流式特性是响应式布局的重要体现。
#### 小结
媒体查询虽然是基于视口的创建响应式布局的主打方式，但它也有弊端，响应式布局同时要结合flexbox一起使用，才能做出更好的响应式布局。参考《精通css》P227。

另外，要做出一个好的响应式设计布局，其实是结合了固定、弹性、流式布局，以流式布局为主体，辅以弹性布局常用的em和rem来设计margin\font-size\padding等等，再辅以固定布局常用到的px来定义必要的元素。(这一段是个人见解，可能不太准确，笔记只有利用em来定义元素的宽高而非margin\font-size\padding才算弹性布局，只有利用px来定义布局元素的宽高才算固定范畴，因此这里所说的可能并非结合了固定和弹性布局，而是使用了固定、弹性布局常用的手段--px和em，即固定常用px，弹性常用em)

## flexbox
参看《flex布局不是布局设计模式》《响应式布局是当前最推荐方式 ---flexbox》《布局的技术手段》

### flex布局不是布局设计模式
参考文首开头的分析，flex布局或flexbox并不是一种布局的设计模式，它不隶属任何一种布局设计方式，它只是一种布局技术手段而已。
它可以被运用于 固定、弹性、响应式布局当中。






