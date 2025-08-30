---
layout: splash
title: "Welcome to Sven Herzberg's Splash Page"
permalink: /splash/   
---


<!--
check out source
[Minimal Mistakes GitHub Repository](https://github.com/mmistakes/minimal-mistakes)

[Minimal Mistakes Splash Page Documentation](https://github.com/mmistakes/minimal-mistakes/blob/master/docs/_pages/splash-page.md)

[Feature Row Include Example](https://github.com/mmistakes/minimal-mistakes/blob/01eeb082da1c3a6abd24a142ac6d2491d91564c2/_includes/feature_row#L4)
-->

V10

<div class="hero">
  <div class="pitch">
    <h1>Hi, I'm Sven</h1>
    <p class="tagline">Developer & AI/ML Enthusiast</p>
    <p>I build performant services, scale prototypes to production, and explore AI & quantum programming.</p>
    <div class="hero__ctas">
      <a class="btn btn--primary" href="/projects/">My Work</a>
      <a class="btn" href="/writing/">Writing</a>
      <a class="btn" href="https://github.com/svenherzberg">GitHub</a>
    </div>
    <div class="badges">
      <span class="badge">16+ yrs experience</span>
      <span class="badge">2 patents filed</span>
      <span class="badge">conference speaker</span>
    </div>
  </div>
  <div class="image">
    <img src="/assets/images/profile.jpeg" alt="Profile Image">
  </div>
</div>

<!-- Add vertical space between the photo and the feature_row content -->
<div style="margin-top: 2rem;"></div>


<!-- PROJECTS -->
<section class="block">
  <div class="block__header">
    <h2>Featured Projects</h2>
  </div>
<div class="feature__wrapper">
  {% assign projects = site.posts | where_exp:"p","p.categories contains 'project'" | slice: 0,6 %}
  {% for post in projects %}
    <div class="feature__item">
      <div class="archive__item">

          <div class="archive__item-teaser">
            <img src="{{ post.thumbnail | relative_url }}"
                 alt="{{ post.title }}">
            {% if f.image_caption %}
              <span class="archive__item-caption">{{ f.image_caption | markdownify | remove: "<p>" | remove: "</p>" }}</span>
            {% endif %}
          </div>

        <div class="archive__item-body">
          {% if post.title %}
            <h2 class="archive__item-title">{{ post.title }}</h2>
          {% endif %}

          {% if post.excerpt %}
            <div class="archive__item-excerpt">
              {{ post.excerpt | markdownify }}
            </div>
          {% endif %}

          {% if post.url %}
            <p><a href="{{ post.url | relative_url }}" class="btn btn--primary">{{ post.btn_label | default: site.data.ui-text[site.locale].more_label | default: "Learn More" }}</a></p>
          {% endif %}
        </div>
      </div>
    </div>
  {% endfor %}
</div>


<!-- ARTICLES -->
<section class="block">
  <div class="block__header">
    <h2>Latest Writings</h2>
  </div>
<div class="feature__wrapper">
  {% assign projects = site.posts | where_exp:"p","p.categories contains 'article'" | slice: 0,6 %}
  {% for post in projects %}
    <div class="feature__item">
      <div class="archive__item">

          <div class="archive__item-teaser">
            <img src="{{ post.thumbnail | relative_url }}"
                 alt="{{ post.title }}">
            {% if f.image_caption %}
              <span class="archive__item-caption">{{ f.image_caption | markdownify | remove: "<p>" | remove: "</p>" }}</span>
            {% endif %}
          </div>

        <div class="archive__item-body">
          {% if post.title %}
            <h2 class="archive__item-title">{{ post.title }}</h2>
          {% endif %}

          {% if post.excerpt %}
            <div class="archive__item-excerpt">
              {{ post.excerpt | markdownify }}
            </div>
          {% endif %}

          {% if post.url %}
            <p><a href="{{ post.url | relative_url }}" class="btn btn--primary">{{ post.btn_label | default: site.data.ui-text[site.locale].more_label | default: "Learn More" }}</a></p>
          {% endif %}
        </div>
      </div>
    </div>
  {% endfor %}

