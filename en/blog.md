---
layout: splash
title: Blog
permalink: /blog
lang: en
---

## Welcome to Blog

<div class="blog-list">
  {% for post in site.posts %}
    <div class="blog-item">
        <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%Y-%m-%d" }}</time>
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </div>
  {% endfor %}
</div>
