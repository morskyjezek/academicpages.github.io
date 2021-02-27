---
layout: archive
title: "Writing"
permalink: /writing/
author_profile: true
redirect_from:
  - /writing
  - /my-writing/
  - /writing.html
---

{% include base_path %}
<!-- Stuff for "related" cards - essays select by topic -->

    <div class="grid__wrapper">
    {% for post in site.posts %}
      {% if post.category = "research funding" limit:4 %}
        {% include archive-single.html type="grid" %}
      {% endif %}
    {% endfor %}
    </div>

<!--  List of "Public writing" -->

  {% for page in site.pages %}
    {% if post.name = "publications.md" %}
      <h2> {% post.title %} </h2>
      
      {% post.content %}

    {% endif %}
    
<!-- List of publications -->
    {% if post.name = "public-writing.md" %}
      <h2> {% post.title%} </h2>

      {% post.content %}

    {% endif %}

  {% endfor %}

