---
layout: page
title: Blog Archive
---

<ol>
{% for post in site.posts %}
  <li><a href="{{post.url}}">{{post.title}}</a> <span class="float-end">{{post.date | date: "%B %Y"}}</span></li>
{% endfor %}
</ol>