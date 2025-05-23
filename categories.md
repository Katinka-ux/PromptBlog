---
layout: page
title: Categories
permalink: /categories/
---

<div class="category-list">
  {% assign categories = site.categories | sort %}
  {% for category in categories %}
    <div class="category-group">
      <h2 class="category-group-title">{{ category[0] }}</h2>
      <ul>
        {% for post in category[1] %}
          <li class="post-item">
            <span class="post-item-date">{{ post.date | date: "%b %d, %Y" }}</span>
            <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
          </li>
        {% endfor %}
      </ul>
    </div>
  {% endfor %}
</div>