---
layout: page
permalink: /categories/
title: Categories
---


<div>
{% for category in site.categories %}
  <div>
    {% capture category_name %}{{ category | first }}{% endcapture %}
    <div id="#{{ category_name | slugize }}"></div>
    <p></p>
    
    <p class="font-weight-bold">{{ category_name }}</p>
    <a name="{{ category_name | slugize }}"></a>
    <ul>
    {% for post in site.categories[category_name] %}
    
      <li> <a href="{{ site.baseurl }}{{ post.url }}">{% if post.title and post.title != "" %}{{post.title}}{% else %}{{post.excerpt |strip_html}}{%endif%}</a></li>
    
    {% endfor %}
    </ul>
  </div>
{% endfor %}
</div>