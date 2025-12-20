---
layout: page
title: Cerca
permalink: /search/
---

<div id="search-container">
    <input type="text" id="search-input" placeholder="Cerca tra le pubblicazioni e gli eventi...">
    <ul id="results-container"></ul>
</div>

<script src="{{ site.baseurl }}/assets/simple-jekyll-search.min.js" type="text/javascript"></script>

<script>
    SimpleJekyllSearch({
    searchInput: document.getElementById('search-input'),
    resultsContainer: document.getElementById('results-container'),
    searchResultTemplate: `<div class="search-result-item">
      <small class="category-tag">{category}</small>
      <a href="{url}">{title}</a>
      <p class="author-hint">di {author}</p>
    </div>`,
    json: '{{ site.baseurl }}/search.json'
    });
</script>