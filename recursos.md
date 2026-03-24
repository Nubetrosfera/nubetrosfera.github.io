---
layout: default
title: Recursos
permalink: /recursos/
---

<h2 style="font-weight: 800; letter-spacing: -1px; margin-bottom: 10px;">biblioteca de recursos 📚</h2>

<div class="grid-cards">
  {% for post in site.categories.recursos %}
    <a href="{{ post.url | relative_url }}" class="card">
      {% if post.image %}
        <img src="{{ site.baseurl }}/{{ post.image }}" class="card-image" alt="{{ post.title }}">
      {% else %}
        <div class="card-image"></div> {% endif %}
      
      <span class="card-meta">{{ post.date | date: "%d %b %Y" }}</span>
      <h3 class="card-title-text">{{ post.title }}</h3>
    </a>
  {% else %}
    <p style="color: #666; font-style: italic;">estamos procesando los datos... pronto habrá scripts disponibles.</p>
  {% endfor %}
</div>