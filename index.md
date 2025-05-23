---
layout: default
title: Home
---

<div class="hero">
  <div class="container">
    <h1>Master the Art of Prompt Engineering</h1>
    <p class="subtitle">Learn advanced techniques, best practices, and cutting-edge strategies to get the most out of AI language models</p>
    <div class="hero-buttons">
      <a href="#latest-posts" class="btn btn-primary">Start Learning</a>
      <a href="/about.html" class="btn btn-secondary">About This Blog</a>
    </div>
  </div>
</div>

<section class="featured-content">
  <div class="container">
    <h2>Latest Posts</h2>
    <div class="posts-grid" id="latest-posts">
      {% for post in site.posts limit:6 %}
        <article class="post-card">
          <div class="post-card-content">
            <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
            <p class="post-meta">
              <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%B %d, %Y" }}</time>
              {% if post.categories.size > 0 %}
                <span class="separator">•</span>
                {% for category in post.categories %}
                  <span class="category">{{ category }}</span>
                {% endfor %}
              {% endif %}
            </p>
            <p class="post-excerpt">{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
            <a href="{{ post.url | relative_url }}" class="read-more">Read More →</a>
          </div>
        </article>
      {% endfor %}
    </div>
    
    <div class="view-all-posts">
      <a href="/categories.html" class="btn btn-outline">View All Posts</a>
    </div>
  </div>
</section>

<section class="features">
  <div class="container">
    <div class="features-grid">
      <div class="feature">
        <h3>🎯 Practical Techniques</h3>
        <p>Learn proven prompt engineering strategies with real-world examples and case studies.</p>
      </div>
      <div class="feature">
        <h3>🎥 Video Tutorials</h3>
        <p>Watch step-by-step demonstrations of advanced prompting techniques in action.</p>
      </div>
      <div class="feature">
        <h3>🔍 Searchable Content</h3>
        <p>Quickly find specific techniques and topics with our powerful search functionality.</p>
      </div>
      <div class="feature">
        <h3>📚 Comprehensive Guides</h3>
        <p>From beginner basics to advanced strategies, we cover every aspect of prompt engineering.</p>
      </div>
    </div>
  </div>
</section>