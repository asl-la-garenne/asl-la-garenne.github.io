---
layout: default
title: Mise à jour des statuts
permalink: /projets/status/
---

<h1>Mise à jour des statuts</h1>
<p>Le conseil syndical propose de mettre à jour les statuts de l'ASL. Ce projet sera soumis au vote lors de la prochaine assemblée générale.</p>

<h2>Pourquoi cette mise à jour est nécessaire</h2>
<p>Nos statuts font encore référence à la loi du 21 juin 1865. Une loi de 2004, complétée par un décret de 2006, impose désormais aux associations comme la nôtre de mettre leurs statuts en conformité. Cette régularisation est urgente, car nos décisions pourraient être plus facilement contestées et l'association pourrait rencontrer des difficultés pour agir en justice.</p>

<h2>Ce qui change</h2>
<p>L'esprit de l'association reste le même : nous continuons à gérer ensemble nos espaces verts communs. Le projet actualise les références légales et clarifie le fonctionnement de l'association, notamment le rôle du bureau et les règles de vote.</p>

<h2>Votre participation est indispensable</h2>
<p>Le vote ne pourra être valable que si un quorum de 2/3 des membres est réuni. Merci de venir à l'assemblée générale ou, si vous ne pouvez pas vous déplacer, de donner votre pouvoir à un autre membre de l'ASL. Chaque voix compte.</p>

<p>Le projet est présenté en huit articles :</p>

<ol class="article-list">
  {% assign statutes = "01|Objet de l'association,02|Membres,03|Assemblée générale,04|Conseil syndical,05|Bureau,06|Finances,07|Modification des statuts,08|Dispositions finales" | split: "," %}
  {% for statute in statutes %}
    {% assign details = statute | split: "|" %}
    <li><a href="{{ '/projets/status/statuts-' | append: details[0] | append: '.html' | relative_url }}">Article {{ forloop.index }} — {{ details[1] }}</a></li>
  {% endfor %}
</ol>
