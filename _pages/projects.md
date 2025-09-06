---
layout: archive
title: Projects
permalink: /projects/
---

<div class="grid cards">
  {% assign projects = site.posts | where_exp:"p","p.categories contains 'project'" %}
  {% for post in projects %}
    <article class="card">
      <a class="card__media" href="{{ post.url | relative_url }}">
        {% if post.thumbnail %}
          <img src="{{ post.thumbnail | relative_url }}" alt="{{ post.title }}" loading="lazy">
        {% else %}
          <div class="card__placeholder">Project</div>
        {% endif %}
      </a>
      <div class="card__body">
        <h3 class="card__title"><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
        <p class="card__excerpt">{{ post.excerpt | strip_html | truncate: 120 }}</p>
      </div>
    </article>
  {% endfor %}
</div>