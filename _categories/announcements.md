---
layout: page
title: Site Announcements
---

<ol>
{% for post in site.posts %}
  {% for category in post.categories %}
  {% if category == "announcements" %}
  <li><a class="lead fw-bold" href="{{post.url}}">{{post.title}}</a></li>
  {% endif %}
  {% endfor %}
{% endfor %}
</ol>