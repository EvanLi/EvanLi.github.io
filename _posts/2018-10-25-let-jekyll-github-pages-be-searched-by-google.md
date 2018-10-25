---
layout: post
title: 让Google搜索到用Jekyll搭建在Github Pages上的博客
date: 2018-10-25
categories: blog
tags: [jekyll,SEO]
description: 让Google搜索到用Jekyll搭建在Github Pages上的博客,提交Google收录，并添加网站地图sitemap
---


# 让Google搜索到用Jekyll搭建在Github Pages上的博客

## 1.查看是否被收录

首先查看你的博客地址是否已经被Google收录，在Google的搜索栏中搜索：

> site:https://xxxx.github.io

其中`https://xxxx.github.io`为你的博客地址，如果结果是`尝试使用Google Search Console`，则意味着没有被收录。

如果搜索出你想要的结果，那么不用继续往下看了。

## 2.搜索资源提交

进入Google Web Master，点击：<a href="https://www.google.com/webmasters/tools/home?hl=zh-CN" target="_blank">Google Search Console</a>（若未登录谷歌账号，需要先登录谷歌账号）

点击添加，提交你的博客网址，然后跳转到如下界面进行验证。

这里需要验证网站所有权，有多种方法进行验证，网站给我们提示了一个推荐验证方法是：通过在你的网站上添加一个它提供的html文件来验证。

![verify-method](/img/20181025/verify-method.jpg)

下载该文件，上传到你的Github Pages的根目录，然后点击验证，即可通过验证。

![verify-completed](/img/20181025/verify-completed.jpg)

或者也可通过其他方法进行验证，比如不想在根目录添加html文件的话，可以选择在网站首页添加元标记，即在_includes目录下的head.html中的head标签之间添加如下元标记即可。

![other-verify-method](/img/20181025/other-verify-method.jpg)

## 3.添加站点地图

站点地图(Site Map)是用来注明网站结构的文件，我们希望搜索引擎的爬虫了解我们的网站结构,以便于高效爬取内容，快速建立索引。

- 点击进入 <a href="https://www.xml-sitemaps.com/" target="_blank">XML-Sitemaps.com</a> 页面，输入博客地址，点击 start。

![xml-sitemaps-com](/img/20181025/xml-sitemaps-com.jpg)

- 等待搜索完成，点击 VIEW SITEMAP DETAILS。

![sitemap-completed](/img/20181025/sitemap-completed.jpg)

- 下载 SITEMAP 文件sitemap.xml并将其上传到网站的根目录。

![download-sitemap](/img/20181025/download-sitemap.jpg)

- 在 Google Search console 中添加你的 sitemap URL。

还是刚刚的<a href="https://www.google.com/webmasters/tools/home?hl=zh-CN" target="_blank">Google Search Console</a>网站，点击刚刚验证成功的你的网站进入控制台，在左边侧边栏“抓取”下找到“站点地图”：

![google-search-console-sitemap](/img/20181025/google-search-console-sitemap.jpg)

点击“添加/测试站点地图”，将https://xxxx.github.io/sitemap.xml提交并刷新，就可以看到博客的网站结构了。

![google-search-console-add-sitemap](/img/20181025/google-search-console-add-sitemap.jpg)


如果没有什么问题的话，到这里就结束了，但是现在用Google还不能立即查到博客的内容，要等到搜索引擎下一次更新检索时才会有显示。

---

**References:**

[1] <a href="https://jactor-sue.github.io/zh-CN/how-blog-on-githubpages-can-be-searched-by-google/" target="_blank">让Google搜索到搭建在Github Pages上的博客</a>

[2] <a href="http://gracegreat1.me/2017/11/%E4%B8%BA%E8%87%AA%E5%B7%B1%E7%9A%84%E5%8D%9A%E5%AE%A2%E6%B7%BB%E5%8A%A0%E6%90%9C%E7%B4%A2%E5%BC%95%E6%93%8E-Google-%E6%94%B6%E5%BD%95-%E4%BB%A5-Namecheap-%E4%B8%BA%E4%BE%8B/" target="_blank">为自己的博客添加搜索引擎（Google）收录（以Namecheap为例）</a>

[3] <a href="https://www.google.com/webmasters/tools/home?hl=zh-CN" target="_blank">Google Search Console</a>