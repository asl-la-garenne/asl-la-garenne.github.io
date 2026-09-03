---
layout: default
title: Mise à jour des statuts
permalink: /projets/status/
---

<h1>Mise à jour des statuts</h1>
<p>Le projet de mise à jour des statuts est présenté en huit articles.</p>

<ol class="article-list">
  {% assign statutes = "01|Objet de l'association,02|Membres,03|Assemblée générale,04|Conseil syndical,05|Bureau,06|Finances,07|Modification des statuts,08|Dispositions finales" | split: "," %}
  {% for statute in statutes %}
    {% assign details = statute | split: "|" %}
    <li><a href="{{ '/projets/status/statuts-' | append: details[0] | append: '.html' | relative_url }}">Article {{ forloop.index }} — {{ details[1] }}</a></li>
  {% endfor %}
</ol>
