---
layout: default
title: "Romanticismo"
---

<h1>Articoli sul Romanticismo</h1>
<p>Tutti gli articoli dedicati al periodo romantico.</p>

<ul>
  {% for post in site.posts %}
    {% if post.categories contains "romanticismo" %}
      <li>
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a> - {{ post.date | date: "%d/%m/%Y" }}
      </li>
    {% endif %}
  {% endfor %}
</ul>
