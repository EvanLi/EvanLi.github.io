---
layout: post
title: 添加MathJax
date: 2015-3-01
categories: note
tags: [Latex,Jekyll]
description: Jekyll中使用MathJax
---


# Jekyll中使用MathJax

在网页中使用latex最流行的解决方案应该是MathJax。这是一个基于JavaScript的Latex渲染引擎，它将网页中的Latex公式转变成多个不同字体的文字或图片的组合。

在Github的Page中使用数学公式，也就是在Jekyll中使用数学公式，MathJax似乎是唯一的选择。

唯一担心的是，Latex中的一些符号，比如下划线会与Markdown中的下划线冲突，但似乎实用过程中又没遇到什么问题。

## 第一步，将`_config.yml`中的markdown修改为

```
markdown: kramdown
```

本地使用jekyll时可能需要额外安装kramdown

```
gem install kramdown
```

kramdown是一个Markdown解析器，它能够正确解释公式内部的符号，不会与Markdown语法冲突，比如不会将`^`符号变成`<sup></sup>`标签。

## 第二步，在header中添加引用和设置代码

也就是`_include/header.html`中添加以下两行代码：

```
<script type="text/x-mathjax-config">MathJax.Hub.Config({tex2jax: {inlineMath: [['$','$'], ['\\(','\\)']]}});</script>
<script type="text/javascript" async src="//cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-MML-AM_CHTML"></script>
```

## 第三步，在Markdown中使用Latex数学公式

**比如行内公式：**

```
$E=mc^2$ is an inline formula.
```
显示结果：

$E=mc^2$ is an inline formula.

**比如行间公式(Lorentz方程)：**

```
$$
\begin{aligned}
\dot{x} &= \sigma(y-x) \\
\dot{y} &= \rho x - y - xz \\
\dot{z} &= -\beta z + xy \\
\end{aligned}
$$
```
显示结果：

$$
\begin{aligned}
\dot{x} &= \sigma(y-x) \\
\dot{y} &= \rho x - y - xz \\
\dot{z} &= -\beta z + xy \\
\end{aligned}
$$

注意，行间公式前后应该都留空行，使得公式能够居中显示。

另外，kramdown的latex语法行内和行间公式是`$`(或`$$`）符号作为分隔符。虽然和一般的使用习惯不同，但是可以保证`_`, `^`, `\`之类符号能够正确解析。

---

**References:**

[1] [Jekyll中使用MathJax](http://pkuwwt.github.io/linux/2013-12-03-jekyll-using-mathjax/)(有删改)
