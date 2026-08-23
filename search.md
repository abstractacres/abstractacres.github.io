---
layout: page
title: Search
permalink: /search/
---

<div id="search-container">
  <input type="text" id="search-input" placeholder="Type to search posts...">
  <ul id="results-container"></ul>
</div>

<!-- Include Simple-Jekyll-Search script from a CDN -->
<script src="https://unpkg.com/simple-jekyll-search@latest/dest/simple-jekyll-search.min.js"></script>

<!-- The initialization code from your screenshot -->
<script>
  var sjs = SimpleJekyllSearch({
    searchInput: document.getElementById('search-input'),
    resultsContainer: document.getElementById('results-container'),
    json: '{{ "/search.json" | relative_url }}',
    searchResultTemplate: '<li><a href="{url}">{title}</a></li>',
    noResultsText: 'No results found',
    limit: 10
  })
</script>
