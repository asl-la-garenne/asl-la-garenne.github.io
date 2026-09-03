---
layout: default
title: Actualités
---

<section aria-labelledby="titre-actualites">
  <h1 id="titre-actualites">Actualités</h1>
  {% for post in site.posts %}
    <article class="content-card">
      <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
      <div class="post-preview">
        {{ post.content }}
      </div>
      <a class="read-more" href="{{ post.url | relative_url }}">Lire la suite</a>
    </article>
  {% endfor %}
</section>
