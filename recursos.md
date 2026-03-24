---
layout: default
title: recursos
permalink: /recursos/
---

<h2 style="font-weight: 800; letter-spacing: -1px; margin-bottom: 30px;">biblioteca de recursos 📊</h2>

<div class="grid-cards">
  {% for post in site.categories.recursos %}
    <a href="{{ post.url | relative_url }}" class="card-item">
      <div class="card-img-container">
        {% if post.image %}
          <img src="{{ site.baseurl }}/{{ post.image }}" alt="{{ post.title }}">
        {% else %}
          <div style="width:100%; height:100%; background: #f8f9fa; display:flex; align-items:center; justify-content:center; font-size: 2rem;">💻</div>
        {% endif %}
      </div>
      <span class="card-meta">{{ post.date | date: "%d %b %Y" }}</span>
      <h3 class="card-title-text">{{ post.title | downcase }}</h3>
    </a>
  {% else %}
    <p style="color: #666; font-style: italic;">procesando datos... pronto encontrarás scripts y protocolos aquí.</p>
  {% endfor %}
</div>