---
layout: home
title: Home Page
---

<h1 class="pb-4 mb-4 fst-italic">From the Editor...</h1>
<p class="lead mb-5">This site is in the beginning stages, if you would like an account email me and I will set you up with one. The posts below are weekly parsha thoughts submitted by users to other sites until I create enough content, I will use a different color background to help people identify the posts. Light green backgrounds are for site announcements. If you would like to run an advertisement on the site get in touch via the contact page or the email link in the sidebar.</p>


{% for post in site.posts %}
  {% for category in post.categories %}

  {% if category == "announcements" %}
  <article class="blog-post alert alert-success">
    <sup class="float-end badge bg-success fw-bold">#{{post.tags}}</sup>
    <h2 class="blog-post-title mb-1">{{post.title}}</h2>
    <p class="blog-post-meta">{{post.date | date: "%B %d, %Y" }} by <a href="{{ '/authors/' | absolute_url }}{{post.author}}">{{post.author}}</a></p>
    <hr/>
    <p>{{post.excerpt}}</p>
    <p><a href="{{post.url}}" class="btn btn-success">Read More...</a></p>
  </article>
  {% endif %}

  {% if category == "torah" %}
  <article class="blog-post bg-white p-3 border border-secondary-subtle rounded">
    <sup class="float-end badge bg-secondary fw-bold">#{{post.tags}}</sup>
    <h2 class="blog-post-title mb-1">{{post.title}}</h2>
    <p class="blog-post-meta">{{post.date | date: "%B %d, %Y" }} by <a href="{{ '/authors/' | absolute_url }}{{post.author}}">{{post.author}}</a></p>
    <hr/>
    <p>{{post.excerpt}}</p>
    <p><a href="{{post.url}}" class="btn btn-outline-secondary">Read More...</a></p>
  </article>
  {% endif %}

  {% if category == "israel" %}
  <article class="blog-post bg-white p-3 border border-secondary-subtle rounded">
    <sup class="float-end badge bg-primary fw-bold">#{{post.tags}}</sup>
    <h2 class="blog-post-title mb-1">{{post.title}}</h2>
    <p class="blog-post-meta">{{post.date | date: "%B %d, %Y" }} by <a href="{{ '/authors/' | absolute_url }}{{post.author}}">{{post.author}}</a></p>
    <hr/>
    <p>{{post.excerpt}}</p>
    <p><a href="{{post.url}}" class="btn btn-outline-primary">Read More...</a></p>
  </article>
  {% endif %}
  
  {% if category == "hassidut" %}
  <article class="blog-post bg-white p-3 border border-secondary-subtle rounded">
    <sup class="float-end badge bg-dark fw-bold">#{{post.tags}}</sup>
    <h2 class="blog-post-title mb-1">{{post.title}}</h2>
    <p class="blog-post-meta">{{post.date | date: "%B %d, %Y" }} by <a href="{{ '/authors/' | absolute_url }}{{post.author}}">{{post.author}}</a></p>
    <hr/>
    <p>{{post.excerpt}}</p>
    <p><a href="{{post.url}}" class="btn btn-outline-dark">Read More...</a></p>
  </article>
  {% endif %}

  {% if category == "teshuvah" %}
  <article class="blog-post bg-white p-3 border border-secondary-subtle rounded">
    <sup class="float-end badge bg-warning fw-bold">#{{post.tags}}</sup>
    <h2 class="blog-post-title mb-1">{{post.title}}</h2>
    <p class="blog-post-meta">{{post.date | date: "%B %d, %Y" }} by <a href="{{ '/authors/' | absolute_url }}{{post.author}}">{{post.author}}</a></p>
    <hr/>
    <p>{{post.excerpt}}</p>
    <p><a href="{{post.url}}" class="btn btn-outline-warning">Read More...</a></p>
  </article>
  {% endif %}

  {% endfor %}
{% endfor %}