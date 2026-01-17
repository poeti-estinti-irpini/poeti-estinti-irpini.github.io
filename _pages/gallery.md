---
layout: page
title: Galleria fotografica
permalink: /gallery/
---

<div class="image-gallery">
  {% for item in site.data.gallery %}
    <div class="gallery-item">
      <img src="{{ item.image_path | relative_url }}" alt="{{ item.title }}">
      <div class="gallery-overlay">
        <div class="gallery-text">
          <h3>{{ item.title }}</h3>
          <p>{{ item.description }}</p>
        </div>
      </div>
    </div>
  {% endfor %}
</div>

<script>
  document.querySelectorAll('.gallery-item').forEach(item => {
    item.addEventListener('click', () => {
      window.open(item.querySelector('img').src, '_blank');
    });
  });
</script>