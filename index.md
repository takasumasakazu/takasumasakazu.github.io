---
layout: home
title: Home
---
# {{ site.title }}

{{ site.description }}

## 最新記事

<ul class="post-list">
  {% for post in site.posts limit:15 %}
    <li>
      <h3>
        <a class="post-link" href="{{ post.url | relative_url }}">
          {{ post.title | escape }}
        </a>
      </h3>
      <span class="post-meta">
        {{ post.date | date: "%Y年%m月%d日" }}
        {% if post.medium_id %}
          • <a href="https://medium.com/p/{{ post.medium_id }}" target="_blank" rel="noopener">
              Medium元記事
            </a>
        {% endif %}
      </span>
      {% if post.excerpt %}
        <div class="post-excerpt">
          {{ post.excerpt | strip_html | truncate: 200 }}
        </div>
      {% endif %}
    </li>
  {% endfor %}
</ul>

<p><a href="/archive/">すべての記事を見る ({{ site.posts.size }}記事)</a></p>
