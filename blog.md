---
layout: default
title: blog
permalink: /blog/
---

<h2 style="font-weight: 800; letter-spacing: -1px; margin-bottom: 30px;">notas y pensamientos ✍️</h2>

<div class="grid-cards">
  {% assign blog_posts = site.posts | where: "categories", "blog" %}
  {% for post in blog_posts %}
    <a href="{{ post.url | relative_url }}" class="card-item">
      <div class="card-img-container">
        {% if post.image %}
          <img src="{{ site.baseurl }}/{{ post.image }}" alt="{{ post.title }}">
        {% else %}
          <div style="width:100%; height:100%; background: #f0f0f0;"></div>
        {% endif %}
      </div>
      <span class="card-meta">{{ post.date | date: "%d %b %Y" }}</span>
      <h3 class="card-title-text">{{ post.title | downcase }}</h3>
    </a>
  {% else %}
    <p style="color: #666; font-style: italic;">el cielo está despejado por ahora...</p>
  {% endfor %}
</div>