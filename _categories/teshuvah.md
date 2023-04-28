---
layout: page
title: Stories of Teshuvah by Baalei Teshuvah
---

<ol>
{% for post in site.posts %}
  {% for category in post.categories %}
  {% if category == "teshuvah" %}
  <li><a class="lead fw-bold" href="{{post.url}}">{{post.title}}</a></li>
  {% endif %}
  {% endfor %}
{% endfor %}
</ol>