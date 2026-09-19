---
layout: default
title: "Home"
---

<section class="latest-news-section">
  <h2 class="section-title" style="font-size: 1.3em; font-weight: normal; font-style: normal; margin-bottom: 10px;">Latest News</h2>
  
  <div class="home-announcement" style="text-align: center; margin: 15px auto; padding: 10px; border-top: 1px solid #eee; border-bottom: 1px solid #eee;">
    <p style="font-style: italic; font-size: 1.2em;">🕯️ Ci sarà un nuovo post una volta a settimana e qualche sorpresa extra! 🕯️</p>
  </div>

  <div class="posts-grid">
    {% for post in site.posts %}
      <article class="post-card">
        
        <!-- Mostra l'immagine del post solo se esiste -->
        {% if post.image %}
          <a href="{{ post.url | relative_url }}" class="post-card-image-wrapper">
            <img src="{{ post.image | relative_url }}" alt="{{ post.title }}" class="post-card-image">
          </a>
        {% endif %}

        <!-- Informazioni sul post -->
        <div class="post-card-content">
          {% if post.category %}
            <span class="post-card-category">{{ post.category }}</span>
          {% endif %}
          <h3 class="post-card-title">
            <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
          </h3>
          <p class="post-card-date">{{ post.date | date: "%d/%m/%Y" }}</p>
        </div>

      </article>
    {% else %}
      <p>Nessun articolo pubblicato finora.</p>
    {% endfor %}
  </div>
</section>
