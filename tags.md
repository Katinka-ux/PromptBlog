---
layout: page
title: Tags
permalink: /tags/
---

<div class="tag-list">
  {% assign tags = site.tags | sort %}
  {% for tag in tags %}
    <div class="tag-group">
      <h2 class="tag-group-title">#{{ tag[0] }}</h2>
      <ul>
        {% for post in tag[1] %}
          <li class="post-item">
            <span class="post-item-date">{{ post.date | date: "%b %d, %Y" }}</span>
            <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
          </li>
        {% endfor %}
      </ul>
    </div>
  {% endfor %}
</div>