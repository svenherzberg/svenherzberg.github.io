---
layout: splash
title: ""
classes: wide
permalink: /
description: "Developer · AI/ML · Performance · Quantum Programming"
author_profile: false
toc: false
---
<div class="hero">
  <div class="pitch">
    <h1>Hi, I'm Sven</h1>
    <p class="tagline">Developer & AI/ML Enthusiast</p>
    <p>I build performant services, scale prototypes to production, and explore AI & quantum programming.</p>
    <div class="badges">
      <span class="badge">16+ yrs experience</span>
      <span class="badge">2 patents filed</span>
      <span class="badge">conference speaker</span>
      
    </div>
  </div>
  <div class="image">
    <img src="/assets/images/sven2.jpg" alt="Profile Image">
  </div>
</div>

<!--
Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet. Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet.Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet. Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet.Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet. Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet.Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet. Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet.Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet. Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet.Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet. Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet.
-->

<!-- PROJECTS -->
<section class="block">
  <div class="block__header">
    <h2>Featured Projects</h2>
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
      </article>
    {% endfor %}
  </div>
</section>

<!-- ARTICLES -->
<section class="block">
  <div class="block__header">
    <h2>Latest Writings</h2>
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
      </article>
    {% endfor %}
  </div>
</section>
