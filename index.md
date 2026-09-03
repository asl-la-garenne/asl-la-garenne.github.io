---
layout: default
title: ASL La Garenne
---

<section id="asl" class="intro" aria-labelledby="titre">
  <h1 id="titre">Bienvenue à l'ASL La Garenne</h1>
  <p>L'Association Syndicale Libre (ASL) La Garenne réunit les propriétaires du lotissement. Elle veille à la gestion, à l'entretien et à la préservation des intérêts communs du quartier.</p>
  <p>Ce site rassemble les informations utiles, les projets en cours et les actualités de l'association.</p>
</section>

<section id="projets" aria-labelledby="titre-projets">
  <h2 id="titre-projets">Projets</h2>
  <p><a href="{{ '/projets/' | relative_url }}">Voir les projets</a></p>
</section>

<section id="actualites" aria-labelledby="titre-actualites">
  <h2 id="titre-actualites">Actualités</h2>
  {% for post in site.posts %}
    <article class="content-card">
      <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
      <p class="post-date"><time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%-d %B %Y" }}</time></p>
      {{ post.excerpt }}
    </article>
  {% endfor %}
</section>
