---
layout: page
title: 記事アーカイブ
permalink: /archive/
---
# 記事アーカイブ

全{{ site.posts.size }}記事

{% assign posts_by_year = site.posts | group_by_exp: "post", "post.date | date: '%Y'" %}
{% for year in posts_by_year %}
## {{ year.name }}年 ({{ year.items.size }}記事)

<ul>
{% for post in year.items %}
  <li>
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
    <span class="post-date">{{ post.date | date: "%m月%d日" }}</span>
  </li>
{% endfor %}
</ul>
{% endfor %}
