---
layout: page
title: "Note"
description: "个人笔记"
header-img: "img/twitter.jpg"
---

## 文章列表

<ul class="listing">
{% for post in site.posts %}
    {% if post.categories contains 'note' %}
        {% capture y %}{{post.date | date:"%Y"}}{% endcapture %}
        {% if year != y %}
        {% assign year = y %}
        <li class="listing-seperator">{{ y }}</li>
        {% endif %}
        <li class="listing-item">
        <time datetime="{{ post.date | date:"%Y-%m-%d" }}">{{ post.date | date:"%Y-%m-%d" }}</time>
        <a href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a>
        </li>
    {% endif %}
{% endfor %}
</ul>

## 标签列表

<div id='tag_cloud'>
{% for tag in site.tags %}
{% for post in tag[1] %}{% if post.categories contains 'note' %}
    <a href="#{{ tag[0] }}" title="{{ tag[0] }}" rel="{{ tag[1].size }}">{{ tag[0] }}</a>
{% endif %}{% endfor %}
{% endfor %}
</div>


<ul class="listing">
{% for tag in site.tags %}
    {% for post in tag[1] %}{% if post.categories contains 'note' %}
        <li class="listing-seperator" id="{{ tag[0] }}">{{ tag[0] }}</li>
    {% endif %}{% endfor %}
    {% for post in tag[1] %}{% if post.categories contains 'note' %}
        <li class="listing-item">
        <time datetime="{{ post.date | date:"%Y-%m-%d" }}">{{ post.date | date:"%Y-%m-%d" }}</time>
        <a href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a>
        </li>
    {% endif %}{% endfor %}
{% endfor %}
</ul>

<script src="/media/js/jquery.tagcloud.js" type="text/javascript" charset="utf-8"></script>
<script language="javascript">
$.fn.tagcloud.defaults = {
    size: {start: 1, end: 1, unit: 'em'},
      color: {start: '#f8e0e6', end: '#ff3333'}
};

$(function () {
    $('#tag_cloud a').tagcloud();
});
</script>
