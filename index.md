---
layout: page
permalink: /
---

<style>
  /* --- 1. CABECERA: Logo y Menú Centrados --- */
  header.site-header .wrapper {
    display: flex !important;
    flex-direction: column !important; /* Logo arriba, menú abajo */
    align-items: center !important;    /* Centra ambos horizontalmente */
    gap: 15px !important;              /* Espacio entre logo y botones */
    padding: 30px 0 !important;
    border: none !important;           /* Quita la línea gris de arriba */
  }

  .site-title {
    font-weight: 800 !important;
    letter-spacing: -1px;
    text-transform: lowercase;
    margin: 0 !important;
    font-size: 1.2rem !important;
  }

  .site-nav {
    display: flex !important;
    justify-content: center !important; /* Centra los botones */
    width: 100% !important;
  }

  .site-nav .nav-link {
    font-family: -apple-system, sans-serif;
    text-transform: lowercase;
    font-size: 14px;
    font-weight: 500;
    letter-spacing: 0.5px;
    color: #555 !important;
    margin: 0 15px !important; /* Espacio equilibrado a los lados */
  }

  .site-nav .nav-link:hover {
    color: #000 !important;
    text-decoration: none;
  }

  /* --- 2. BIENVENIDA: Foto más grande que el texto --- */
  .grid-welcome {
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    gap: 60px; /* Un poco más de aire entre columnas */
    margin: 40px 0 60px 0;
  }

  .welcome-text {
    flex: 0.8; /* COLUMNA MÁS ANGOSTA */
    min-width: 300px;
    font-family: -apple-system, sans-serif;
    font-size: 25px; 
    font-weight: 700; 
    line-height: 1.1;
    letter-spacing: -1.5px;
    color: #111; 
    max-width: 400px;
  }

  .welcome-photo-container {
    flex: 1.2; /* COLUMNA MÁS ANCHA */
    min-width: 300px;
  }

  .welcome-photo {
    width: 100%;
    height: auto;
    border-radius: 35px;
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