---
layout: page
permalink: /archive/
title: Archivio pubblicazioni
---


<div class="pubblicazioni-grid">
  {% for post in site.posts %}
    <article class="pubblicazione-card card-{{ post.category | slugify }}">
      <div class="card-category">
        {% if post.categories contains "concorso" %} 🏆 Concorso
        {% elsif post.categories contains "eventi" %} 📍 Evento
        {% else %} 📰 Notizia
        {% endif %}
      </div>
      
      <div class="card-content">
        <h2 class="card-title">
          <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
        </h2>
        <p class="card-date">{{ post.date | date: "%-d %B %Y" }}</p>
        <p class="card-excerpt">{{ post.excerpt | strip_html | truncate: 120 }}</p>
      </div>

      <div class="card-footer">
        <a href="{{ post.url | relative_url }}" class="read-more">Leggi tutto →</a>
      </div>
    </article>
  {% endfor %}
</div>
