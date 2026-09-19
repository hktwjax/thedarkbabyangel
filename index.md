---
layout: default
title: "Home"
---

<section class="latest-news-section">
  <h2 class="section-title" style="font-size: 1.45em; font-weight: normal; font-style: normal; margin-bottom: 10px;">Latest News</h2>
  
  <div class="home-announcement" style="text-align: center; margin: 15px auto; padding: 15px 10px;">
    <!-- Immagine superiore: divider5.PNG -->
    <img src="{{ '/assets/images/divider5.PNG' | relative_url }}" alt="decorazione superiore" style="width: 100%; max-width: 650px; height: auto; display: block; margin: 0 auto 10px auto; filter: brightness(0) invert(1); opacity: 0.85;">
    
    <p style="font-style: italic; font-size: 1.05em; margin: 10px 0;">🕯️ Ci sarà un nuovo post una volta a settimana e qualche sorpresa extra! 🕯️</p>
    
    <!-- Immagine inferiore: divider6.PNG -->
    <img src="{{ '/assets/images/divider6.PNG' | relative_url }}" alt="decorazione inferiore" style="width: 100%; max-width: 650px; height: auto; display: block; margin: 10px auto 0 auto; filter: brightness(0) invert(1); opacity: 0.85;">
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
          {% if post.categories %}
            <span class="post-card-category">{{ post.categories }}</span>
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
</section>
