---
title: "Sample Page"
permalink: /sample-page/
<!--layout: single
collection: recipes-->
---

luka
{% for image in site.static_files %}
  {% if image.path contains 'assets/images' %}
    {% unless image.path contains '-th.' %}
      <a href="{{ image.path }}">
        <img src="{{ image.basename | append: '-th' | append: image.extname }}" alt="">
      </a>
    {% endunless %}
  {% endif %}
{% endfor %}
