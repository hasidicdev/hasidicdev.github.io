---
layout: page
title: Eretz Yisrael
---

<ol>
{% for post in site.posts %}
  {% for category in post.categories %}
  {% if category == "israel" %}
  <li><a class="lead fw-bold" href="{{post.url}}">{{post.title}}</a></li>
  {% endif %}
  {% endfor %}
{% endfor %}
</ol>