---
layout: page
permalink: /
---

<div class="grid-welcome">
  <div class="welcome-text">
    
    Bienvenidx a Nubetrosfera.
    En este espacio encontrarás notas y
    recursos de una científica atmosférica
    a quien le fascina la fotografía,
    la meteorología y sobre todo,
    divulgar el conocimiento ☁️.
  </div>

  <div class="welcome-photo-container">
    <img src="{{ site.baseurl }}/assets/images/DSCN0282.JPG" alt="Mañana en Xalapa. Autor: DALM" class="welcome-photo">
  </div>
</div>

<div class="seccion-notas">
  <h2>Últimas Notas ✍️</h2>
  {% for post in site.posts limit:3 %}
    <p style="margin-bottom: 15px;">
      <span style="color: #888; font-size: 0.9rem; margin-right: 15px;">{{ post.date | date: "%b %-d, %Y" }}</span>
      <a href="{{ post.url | relative_url }}" style="font-weight: 600; text-decoration: none; color: #0076ff;">{{ post.title }}</a>
    </p>
  {% endfor %}
</div>