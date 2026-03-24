---
layout: page
title: Inicio
permalink: /
---

<div class="grid-welcome">

  <div class="welcome-text">
    
    Bienvenido a Nubetrosfera. <br>
    En este espacio encontrarás notas y recursos de <br>
    una científica atmosférica a quien le fascina la <br>
    fotografía, la meteorología y sobre todo, divulgar <br>
    el conocimiento. <br>
  </div>

  <div class="welcome-photo-container">
    <img src="{{ site.baseurl }}/assets/images/tu-foto.jpg" alt="Dani López - Meteoróloga" class="welcome-photo">
  </div>

</div>

<h2>Últimas Notas ✍️</h2>
{% for post in site.posts limit:3 %}
  <p>
    <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
  </p>
{% endfor %}