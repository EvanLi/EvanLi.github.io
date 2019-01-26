---
layout: post
title: 谷歌搜索引擎高级搜索、命令大全表格总结(完整示例说明)
date: 2019-01-26
categories: blog
tags: [google,SEO]
description: 谷歌搜索引擎高级搜索技巧，搜索引擎命令大全，用表格进行总结，附有完整示例及说明
---

# 谷歌搜索引擎高级搜索、命令大全表格总结(完整示例及说明)

---

## 1.搜索引擎搜索思路

### (1) 搜索引擎解决思路：

取词，优化，反推，转换。

要学会关键词联想、简化，还要有一个大的思路最重要的是刨根问底的精神，找到最终答案的毅力。

### (2) 每次搜索时都是有意识的、层层推进的而不是盲目的：

**一个完整的“高级信息搜索”过程一定是要包含如下8个完整的步骤：**

分析问题、选择合适的检索工具、提取检索词、构造检索式、进行检索、筛选检索结果、调整检索策略、反思总结。

### (3) 掌握了工具和关键字后，要知道二者如何配合使用:

比如需要查找一份政府文件，如果知道准确的文件名，就可以加半角引号进行精确检索；

但如果不知道准确名称，就可以用site语法只在政府网站内用相关关键字查询，而不是在全网大海捞针。

## 2.搜索引擎命令大全表格总结

|序号|语法|语法说明|示例|示例说明|
|:---|:---|:---|:---|:---|
|1|**+**|同AND，搜索包含多个关键词的结果|搜索 + 引擎|搜索包含【搜索】和【引擎】两个词的页面|
|2|**OR**|或者|搜索 OR 引擎|搜索包含【搜索】或【引擎】两个词的页面|
|3|**-**|减号，不包含减号后面词的页面|搜索引擎 -百度|搜索不包括【百度】的【搜索引擎】的页面|
|4|**“”**|双引号，精确匹配|“搜索引擎”|精确匹配【搜索引擎】这个关键词的页面|
|5|**\***|星号，通配符，模糊搜索，星号代替某个字|搜*引擎|星号可以为任何字|
|6|**@**|在用于搜索社交媒体的字词前加上@|trump @twitter|搜索trump的twitter|
|7|**$**|在数字前加上$搜索特定价格|camera $400|搜索400$的camera|
|8|**#**|搜索 # 标签|#throwbackthursday|搜索标签throwbackthursday|
|9|**..**|两个点，在两个数字之间加上.. 在数字范围内执行搜索|camera $500..$1000|搜索500$-1000$的camera|
|10|**filetype**|搜索某一种文件类型的资源|C++ filetype:pdf|搜索类型为pdf的C++网页资源|
|11|**site**|在指定站点搜索|C++ site:https://www.zhihu.com|在知乎中搜索和C++相关的网页|
|12|**cache**|查看网站的 Google 缓存版本，会直接显示缓存页面|cache:weibo.com|查看微博的谷歌快照|
|13|**info**|在网址前加info:，获取网站详情|info:github.com|搜索github网站详情|
|14|**related**|搜索与某个网站有关联的页面|related:sina.com|和新浪网网站结构内容相似的一些其它网站|
|15|**link**|返回所有链接到某个URL地址的网页|link:www.csdn.net|搜索所有含指向【www.csdn.net】链接的网页|
|16|**inurl**|搜索查询词出现在url 中的页面|inurl:搜索引擎|搜索链接url中有【搜索引擎】的网页|
|17|**intitle**|搜索查询词出现在页面标题(title)中的页面，支持中文和英文|intitle:搜索引擎|搜索页面标题中有【搜索引擎】的网页|
|18|**intext**|搜索查询词出现在页面正文(title)中的页面，支持中文和英文|SEO intext:搜索引擎|在正文包含【搜索引擎】的网页中搜索【SEO】|
|19|**inanchor**|搜索链接锚文字(即链接显示的文字)中包含搜索词的页面|inanchor:前端|搜索链接锚文字中包含【前端】的页面|
|20|**allinurl**|即all+inurl 页面url中包含多个关键词的页面|allinurl:SEO 搜索引擎优化|相当于 ：inurl:SEO inurl:搜索引擎优化|
|21|**allintitle**|即all+intitle 页面标题中包含多个关键词的页面|allintitle:SEO 搜索引擎优化|相当于：intitle:SEO intitle:搜索引擎优化|
|22|**allintext**|即all+inanchor 页面正文包含多个关键词的页面|allintext:SEO 搜索引擎优化|相当于：intext:SEO intext:搜索引擎优化|
|23|**allinanchor**|即all+inanchor 页面链接锚文字包含多个关键词的页面|allinanchor:SEO 搜索引擎优化|相当于：inanchor:SEO inanchor:搜索引擎优化|
|24|**weather**|weather/time/sunrise/sundown+城市名，返回城市的天气/时间/日出时间/日落时间|weather:beijing|显示北京的天气|
|25|**music**|或者用songs，歌手名字+music/songs|周杰伦 music|返回周杰伦的各首歌曲|

_注：_

_1.冒号均为英文状态的；_

_2.冒号后面没有空格；_

_3.命令前面需要用空格隔开，如C++ filetype:pdf，filetype前面有空格；_

## 3.命令组合、搜索结果展示

组合以上的命令，可以得到更精确的结果

如搜索：

```
allintitle:机器学习 入门 site:zhihu.com
```

可以搜索到知乎上所有标题中有机器学习和入门的网页，如下图：

![](/img/20190126/combine1.png)

搜索：

```
allintext:机器学习 深度学习 filetype:pdf
```

可以搜索到所有正文中有机器学习和深度学习字段的pdf文件，如下图：

![](/img/20190126/combine2.png)

---

**References:**

[1] <a href="https://www.zhihu.com/question/19847393" target="_blank">搜索引擎有哪些常用技巧？-知乎</a>

[2] <a href="https://support.google.com/websearch/answer/2466433" target="_blank">谷歌搜索帮助-优化网页搜索</a>