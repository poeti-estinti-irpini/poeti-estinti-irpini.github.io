---
layout: page
permalink: /poesie/
title: Leggi le poesie 
---

<div class="poesie-archive">
  {% assign poesie_ordinate = site.poesie | reverse %}
  {% for poesia in poesie_ordinate %}
    <a href="{{ poesia.url }}" class="poesia-item">
      <div class="poesia-info">
        <span class="poesia-link-title">{{ poesia.title }}</span>
        <span class="poesia-link-author">di {{ poesia.author | default: "I Poeti Estinti" }}</span>
      </div>
      <span class="poesia-link-location">✒️ 📖</span>
    </a>
  {% endfor %}
</div>
