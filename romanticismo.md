---
layout: default
title: "Romanticismo"
permalink: /romanticismo/
---

<div class="theme-art-history">

<section class="category-header">
  <h2>Romanticismo</h2>
</section>

<div class="posts-grid">
  {% for post in site.posts %}
    {% if post.categories contains "romanticismo" %}
      <article class="post-card">
        <div class="post-card-content">
          <span class="post-card-category">Romanticismo</span>
          <h3 class="post-card-title">
            <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
          </h3>
          <span class="post-card-date">{{ post.date | date: "%d/%m/%Y" }}</span>
        </div>
      </article>
    {% endif %}
  {% endfor %}
</div>

<!-- Decorazione in basso a destra (finestra) specifica di Art History -->
<div class="decor-art-history decor-finestra"></div>

</div>
