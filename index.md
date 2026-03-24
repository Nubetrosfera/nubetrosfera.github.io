---
layout: default
permalink: /
---

<div class="grid-welcome">
  <div class="welcome-text">
    Bienvenidx a Nubetrosfera ☁️. 
    En este espacio encontrarás notas y 
    recursos de una científica atmosférica 
    a quien le fascina la fotografía, 
    la meteorología y sobre todo, 
    divulgar el conocimiento.
  </div>

  <div class="welcome-photo-container">
    <img src="{{ site.baseurl }}/assets/images/DSCN0282.JPG" alt="Xalapa" class="welcome-photo">
  </div>
</div>

<div class="seccion-notas">
  <h2 style="font-weight: 800; letter-spacing: -1px; margin-bottom: 30px;">Últimas notas ✍️</h2>
  
  {% for post in site.posts limit:5 %}
    <article style="margin-bottom: 25px; display: flex; align-items: baseline; gap: 20px;">
      <span style="color: #999; font-size: 0.85rem; font-family: monospace; min-width: 100px;">
        {{ post.date | date: "%d %b %Y" | downcase }}
      </span>
      <a href="{{ post.url | relative_url }}" style="font-weight: 600; text-decoration: none; color: #111; font-size: 1.1rem;">
        {{ post.title | downcase }}
      </a>
    </article>
  {% else %}
    <p style="color: #666; font-style: italic;">Aún no hay notas, pero el cielo está preparando algo...</p>
  {% endfor %}
</div>

<style>
  .seccion-notas {
    margin-top: 80px;
    max-width: 800px;
  }
  
  .seccion-notas a:hover {
    color: #0076ff !important;
    text-decoration: underline !important;
  }
</style>