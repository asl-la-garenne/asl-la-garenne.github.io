---
layout: default
title: ASL La Garenne
---

<section id="asl" class="intro" aria-labelledby="titre">
  <h1 id="titre">Bienvenue à l'ASL La Garenne</h1>
  <p>Ce site rassemble les informations utiles, les projets en cours et les actualités de l'association.</p>
</section>

<section id="actualites" aria-labelledby="titre-actualites">
  <h2 id="titre-actualites">Actualités</h2>
  {% for post in site.posts %}
    <article class="content-card">
      <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
      <div class="post-preview">
        {{ post.content }}
      </div>
      <a class="read-more" href="{{ post.url | relative_url }}">Lire la suite</a>
    </article>
  {% endfor %}
</section>
