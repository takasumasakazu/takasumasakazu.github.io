---
layout: page
title: カテゴリ
permalink: /categories/
---
# カテゴリ一覧

{% for category in site.categories %}
## {{ category[0] }} ({{ category[1].size }}記事)

<ul>
{% for post in category[1] %}
  <li>
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
  </li>
{% endfor %}
</ul>
{% endfor %}
