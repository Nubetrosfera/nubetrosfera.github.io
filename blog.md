---
layout: default
title: Blog
permalink: /blog/
---

<h2 style="font-weight: 800; letter-spacing: -1px; margin-bottom: 10px;">Artículos de divulgación 📚</h2>

<div class="grid-cards">
  {% for post in site.categories.blog %}
    <a href="{{ post.url | relative_url }}" class="card">
      {% if post.image %}
        <img src="{{ site.baseurl }}/{{ post.image }}" class="card-image" alt="{{ post.title }}">
      {% else %}
        <div class="card-image"></div> {% endif %}
      
      <span class="card-date">{{ post.date | date: "%d %b %Y" }}</span>
      <h3 class="card-title">{{ post.title }}</h3>
    </a>
  {% else %}
    <p style="color: #666; font-style: italic;">el cielo está despejado... pronto habrá nuevas entradas.</p>
  {% endfor %}
</div>