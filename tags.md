---
layout: page
title: "Tags"
description: "哈哈，你找到了我的文章基因库"
header-img: "img/semantic.jpg"
---

## 本页使用方法

1. 在下面选一个你喜欢的词
2. 点击它
3. 相关的文章会「唰」地一声跳到页面顶端
4. 马上试试？

## 基因列表

<div id='tag_cloud'>
{% for tag in site.tags %}
	<a href="#{{ tag[0] }}" title="{{ tag[0] }}" rel="{{ tag[1].size }}">{{ tag[0] }}</a>
{% endfor %}
</div>


<ul class="listing">
{% for tag in site.tags %}
    <b id = "{{ tag[0] }}">{{ tag[0] }}</b>
	{% for post in tag[1] %}
		<li class="listing-item">
		<time datetime="{{ post.date | date:"%Y-%m-%d" }}">{{ post.date | date:"%Y-%m-%d" }}</time>
		<a href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a>
		</li>
	{% endfor %}
{% endfor %}
</ul>

<script src="/assets/js/jquery.tagcloud.js" type="text/javascript" charset="utf-8"></script>

<script type="text/javascript">
$.fn.tagcloud.defaults = {
  size: {start: 14, end: 18, unit: 'pt'},
  color: {start: '#cde', end: '#f52'}
};
$(function() {
    $('#tag_cloud a').tagcloud();
});
</script>