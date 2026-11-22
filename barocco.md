---
layout: default
title: "Barocco"
permalink: /barocco/
category: "Art History"
---

<section class="category-header">
  <h2>Barocco</h2>
</section>

<div class="posts-grid">
  {% for post in site.posts %}
    {% if post.categories contains "barocco" or post.tags contains "barocco" %}
      <article class="post-card">
        <div class="post-card-content">
          <span class="post-card-category">Barocco</span>
          <h3 class="post-card-title">
            <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
          </h3>
          <span class="post-card-date">{{ post.date | date: "%d/%m/%Y" }}</span>
        </div>
      </article>
    {% endif %}
  {% endfor %}
</div>
