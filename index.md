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
  <article class="content-card" aria-labelledby="statuts">
    <h3 id="statuts">Mise à jour des statuts</h3>
    <p>Le projet de mise à jour des statuts est présenté en huit articles.</p>
    <ol class="article-list">
      {% assign statutes = "01|Objet de l'association,02|Membres,03|Assemblée générale,04|Conseil syndical,05|Bureau,06|Finances,07|Modification des statuts,08|Dispositions finales" | split: "," %}
      {% for statute in statutes %}
        {% assign details = statute | split: "|" %}
        <li><a href="{{ '/statuts-' | append: details[0] | append: '.html' | relative_url }}">Article {{ forloop.index }} — {{ details[1] }}</a></li>
      {% endfor %}
    </ol>
  </article>
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
