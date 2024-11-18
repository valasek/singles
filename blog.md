---
layout: single
title: Blog
permalink: /blog/
---

<div class="blog-posts">
  {% for post in site.posts %}
    <article>
      <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
      <time datetime="{{ post.date | date: '%Y-%m-%d' }}">
        {{ post.date | date: "%B %d, %Y" }}
      </time>
      {% if post.header.image %}
        <img src="{{ post.header.image }}"/>
      {% endif %}
      {% if post.description %}
        <p>{{ post.description }}</p>
      {% endif %}
    </article>
  {% endfor %}
</div>
