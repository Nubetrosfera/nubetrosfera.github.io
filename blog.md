---
layout: default
title: Blog
permalink: /blog/
---
Blog - articulos de divulgación

<div class="grid-cards">
  {% for post in site.posts %}
    <a href="{{ post.url | relative_url }}" class="card">
      {% if post.image %}
        <img src="{{ site.baseurl }}/{{ post.image }}" class="card-image" alt="{{ post.title }}">
      {% else %}
        <div class="card-image"></div> {% endif %}
      
      <span class="card-date">{{ post.date | date: "%d %b %Y" }}</span>
      <h3 class="card-title">{{ post.title }}</h3>
    </a>
  {% endfor %}
</div>