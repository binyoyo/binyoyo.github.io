---
layout: post
title: "坑爹的IE，在z-index的问题"
date: 2013-01-13
categories: blog
description: 写demo的时候遇到，ie6的bug，设置层级z-index不起作用了，网上查阅了些资料，自己记录一下。
---
##CSS中的z-index

在w3c的规范中的z-index

1.元素在 "Z 轴" 方向上的呈现顺序，由层叠上下文和层叠级别决定。在文档中，每个元素仅属于一个层叠上下文。在给定的层叠上下文中，每个元素都有一个整型的层叠级别，它描述了在相同层叠上下文中元素在 "Z轴" 上的显示顺序


2.同一个层叠上下文中，层叠级别大的显示在上，层叠级别小的显示在下，相同层叠级别时，遵循后来居上的原则（back-to-font）

3.不同层叠上下文中，元素显示顺序以父级层叠上下文的层叠级别来决定显示的先后顺序。与自身的层叠级别无关；


CSS中设置z-index来改变层级，其中前提就是元素的position属性要是relative，absolute或是fixed。float会使在z-index失效。

在z-index不起作用可能因为： 

  1.标签有设置浮动
  
  2.父标签为relative

  3.标签没有设置relative，absolute或是fixed

解决的方法有：去除浮动，设置position，父标签改为absolute。

##ie6中的z-index

当定位元素的 'z-index' 未设置时（默认为 auto），在 IE6 IE7 IE8(Q) 下将会创建一个新的局部层叠上下文。而在其它浏览器下，则严格按照规范，不产生新的局部层叠上下文。

IE6下，层级的表现不是看子标签的z-index多高，而要看整个DOM tree的第一个relative属性的父标签的层级。

例如：

```
	<div style="position:relative;" class="1">one
	    <div style="position:absolute; z-index:1;" class="2">two</div>
	</div>
	<div style="position:absolute;" class="3">three</div>
```

在ie6下显示的结果（由高到低）：three->two->one

而在其他浏览器的结果为：two->tree->one

解决方法：在第一relative属性的父标签加上更高的z-index。



