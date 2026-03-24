---
layout: page
permalink: /
---

<style>
  /* --- 1. CABECERA: Logo y Botones en la misma fila --- */
  .site-header .wrapper {
    display: flex !important;
    justify-content: space-between !important;
    align-items: center !important;
    padding: 20px 0 !important;
  }

  .site-title {
    margin-right: auto !important; /* Empuja los botones a la derecha */
    font-size: 1.1rem !important;
    font-weight: 800 !important;
    text-transform: lowercase;
    letter-spacing: -1px;
  }

  .site-nav {
    line-height: 1 !important;
  }

  .site-nav .nav-link {
    text-transform: lowercase;
    font-size: 0.9rem !important;
    font-weight: 500;
    margin-left: 20px !important;
    color: #555 !important;
  }

  /* --- 2. BIENVENIDA: Proporciones Ajustadas --- */
  .grid-welcome {
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    gap: 60px;
    margin: 60px 0;
  }

  .welcome-text {
    flex: 0.8; /* El texto ahora es un poco más pequeño en proporción */
    min-width: 300px;
    font-family: -apple-system, sans-serif;
    font-size: 40px; 
    font-weight: 800; 
    line-height: 1.1;
    letter-spacing: -1.5px;
    color: #111;
  }

  .welcome-photo-container {
    flex: 1.2; /* LA FOTO GANA: Es más grande que el texto */
    min-width: 350px;
  }

  .welcome-photo {
    width: 100%;
    height: auto;
    border-radius: 40px; 
    box-shadow: 0 20px 50px rgba(0,0,0,0.1);
    display: block;
    transition: transform 0.3s ease; /* Un toque extra: se mueve al pasar el mouse */
  }

  .welcome-photo:hover {
    transform: scale(1.02);
  }
</style>

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