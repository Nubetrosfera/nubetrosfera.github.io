---
layout: page
title: Inicio
permalink: /
---

<style>
  .grid-welcome {
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    gap: 40px;
    margin: 40px 0 60px 0;
  }

  .welcome-text {
    flex: 1.5;
    min-width: 300px;
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
    font-size: 42px; /* Tamaño grande impacto */
    font-weight: 800; /* Extra negrita */
    line-height: 1.1;
    letter-spacing: -1.5px;
    color: #111;
  }

  .welcome-photo-container {
    flex: 1;
    min-width: 250px;
  }

  .welcome-photo {
    width: 100%;
    height: auto;
    border-radius: 35px; /* Bordes redondeados modernos */
    box-shadow: 0 15px 35px rgba(0,0,0,0.1);
    display: block;
  }

  .seccion-notas {
    margin-top: 50px;
    border-top: 1px solid #eee;
    padding-top: 30px;
  }
</style>

<div class="grid-welcome">
  <div class="welcome-text">
    
    Bienvenidx a Nubetrosfera ☁️. <br>
    En este espacio encontrarás notas y <br>
    recursos de una científica atmosférica <br>
    a quien le fascina la fotografía, <br>
    la meteorología y sobre todo, <br>
    divulgar el conocimiento. <br>
  </div>
  
  <div class="welcome-photo-container">
    <img src="{{ site.baseurl }}/assets/images/tu-foto.jpg" alt="Dani López" class="welcome-photo">
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