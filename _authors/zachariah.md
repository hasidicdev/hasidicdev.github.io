---
layout: author
title: Author Profile Page
author: zachariah
---

{% for author in site.data.authors %}
  {% if author.id == page.author %}
  <p class="display-4 fw-bold fst-italic">{{author.name}}</p>
  <p class="lead">{{author.bio}}</p>

  <h2>Contact</h2>
  <p>
    <i class="fa-brands fa-discord"></i> <a href="https://discord.gg/{{site.social.invite_link}}" target="_blank">Join On Discord</a><br/>
    
  </p>
  {% endif %}
{% endfor %}

<hr class="col-9" />

### Articles By This Author
<ol>
{% for post in site.posts %}
  {% if post.author == page.author %}
  <li><a href="{{post.url}}">Read Article</a> - "{{post.title}}"</li>
  {% endif %}
{% endfor %}
</ol>