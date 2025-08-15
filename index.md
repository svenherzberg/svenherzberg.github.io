---
layout: single
title: "Sven Herzberg"
classes: wide
permalink: /
description: "Developer · AI/ML · Performance · Quantum Programming"
author_profile: false
toc: false
---

v9


<div class="hero">
  <div class="pitch">
    <h1>Hi, I'm Sven</h1>
    <p class="tagline">Developer & AI/ML Enthusiast</p>
    <p>I build performant services, scale prototypes to production, and explore AI & quantum programming.</p>
    <div class="buttons">
      <a href="#" class="button">My Work</a>
      <a href="#" class="button">Writing</a>
      <a href="#" class="button">GitHub</a>
    </div>
    <div class="badges">
      <span class="badge">16+ yrs experience</span>
      <span class="badge">2 patents filed</span>
      <span class="badge">Conference Speaker</span>
    </div>
  </div>
  <div class="image">
    <img src="/assets/images/profile.jpeg" alt="Profile Image">
  </div>
</div>

<!-- HERO SPLIT -->
<section class="hero-split">
  <div class="hero-split__text">
      <h1>Hi, I'm Sven — Developer & AI/ML Enthusiast</h1>
      <p>I build performant services, scale prototypes to production, and explore AI & quantum programming.</p>

      <div class="badges">
        <span class="badge">16+ yrs experience</span>
        <span class="badge">2 patents filed</span>
        <span class="badge">Conference Speaker</span>
      </div>

      <div class="hero__ctas">
        <a class="btn btn--primary" href="/projects/">My Work</a>
        <a class="btn" href="/writing/">Writing</a>
        <a class="btn" href="https://github.com/YOUR_GH_USERNAME">GitHub</a>
      </div>

      <nav class="quicklinks">
        <a href="/projects/#ml">ML</a>
        <a href="/projects/#performance">Performance</a>
        <a href="/projects/#quantum">Quantum</a>
        <a href="/about/">About</a>
      </nav>

  </div>
</section>

<!-- PROJECTS -->
<section class="block">
  <div class="block__header">
    <h2>Featured Projects</h2>
    <a class="link-more" href="/projects/">View all →</a>
  </div>

  <div class="grid cards">
    {% assign projects = site.posts | where_exp:"p","p.categories contains 'project'" | slice: 0,6 %}
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
        <div class="card__foot">
          {% if post.tags %}<span>#{{ post.tags | join: "  #" }}</span>{% endif %}
        </div>
      </article>
    {% endfor %}
  </div>
</section>

<!-- ARTICLES -->
<section class="block">
  <div class="block__header">
    <h2>Latest Articles</h2>
    <a class="link-more" href="/writing/">More posts →</a>
  </div>

  <div class="grid cards">
    {% assign articles = site.posts | where_exp:"p","p.categories contains 'article'" | slice: 0,6 %}
    {% for post in articles %}
      <article class="card">
        <a class="card__media" href="{{ post.url | relative_url }}">
          {% if post.thumbnail %}
            <img src="{{ post.thumbnail | relative_url }}" alt="{{ post.title }}" loading="lazy">
          {% else %}
            <div class="card__placeholder">Article</div>
          {% endif %}
        </a>
        <div class="card__body">
          <h3 class="card__title"><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
          <p class="card__excerpt">{{ post.excerpt | strip_html | truncate: 120 }}</p>
        </div>
        <div class="card__foot">
          <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%b %d, %Y" }}</time>
        </div>
      </article>
    {% endfor %}
  </div>
</section>