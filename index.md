---
layout: page
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
    font-family: -apple-system, sans-serif;
    font-size: 30px; 
    font-weight: 600; 
    line-height: 1.1;
    letter-spacing: -1.5px;
    color: #111; 
    /* ESTA ES LA MAGIA: */
    max-width: 600px; /* Ajusta este número según qué tan ancho quieras el bloque */
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
/* Ajuste del Menú Superior (Navegación) */
  header.site-header {
    border: none !important; /* Quita la línea gris de arriba */
    padding: 30px 0;
  }

  .site-title {
    font-weight: 800 !important;
    letter-spacing: -1px;
    text-transform: lowercase;
  }

  .site-nav .nav-link {
    font-family: -apple-system, sans-serif;
    text-transform: lowercase; /* Todo en minúsculas como iamrobin */
    font-size: 14px; /* Más pequeño y elegante */
    font-weight: 500;
    letter-spacing: 0.5px;
    color: #555 !important;
    margin-left: 25px;
  }

  /* Cambia el color cuando pasas el mouse */
  .site-nav .nav-link:hover {
    color: #000 !important;
    text-decoration: none;
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