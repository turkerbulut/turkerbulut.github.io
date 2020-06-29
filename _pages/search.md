---
layout: page
title: Search
permalink: /search/
---

<div id="search-container">
    <input type="text" class="form-control" id="search-input" placeholder="Search through the blog posts...">
    <br>
    <ol id="results-container"></ol>
</div>

<script src="{{ site.baseurl }}/assets/simple-jekyll-search.min.js" type="text/javascript"></script>

<script>
    SimpleJekyllSearch({
    searchInput: document.getElementById('search-input'),
    resultsContainer: document.getElementById('results-container'),
    searchResultTemplate: '<li> <span> <a href="{url}"><p>{title}</p></a> </span></li>',
    json: '{{ site.baseurl }}/search.json'
    });
</script>