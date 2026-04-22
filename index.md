---
layout: default
title: ""
description: Personal hub for projects, tools, experiments, and other things built by Rait Nigol.
permalink: /
---

<div class="home-intro">
  <p class="home-lead">
    Personal hub for projects, tools, experiments, and other things I build.
  </p>

  <div class="home-cta">
    <a class="cta-button cta-primary" href="/projects/">View Projects</a>
    <a class="cta-button cta-secondary" href="/about/">About</a>
  </div>

  <div class="social-links">
    {% for social in site.data.socials %}
      <a
        class="social-link"
        href="{{ social.url }}"
        target="_blank"
        rel="noopener noreferrer"
        aria-label="{{ social.name }}"
        title="{{ social.name }}"
      >
        <i class="fa-brands fa-{{ social.icon }}"></i>
      </a>
    {% endfor %}
  </div>
</div>

<h2>Featured repositories</h2>

<div class="repo-grid">
  {% assign repos = site.data.repos | where: "featured", true | sort: "priority" %}
  {% for repo in repos %}
    <article class="repo-card">
      <h3 class="repo-title">
        <a href="{{ repo.url }}" target="_blank" rel="noopener noreferrer">{{ repo.name }}</a>
      </h3>

      <p class="repo-description">{{ repo.description }}</p>

      {% if repo.tags %}
        <div class="repo-tags">
          {% for tag in repo.tags %}
            <span class="tag tag-{{ tag | slugify }}">{{ tag }}</span>
          {% endfor %}
        </div>
      {% endif %}
    </article>
  {% endfor %}
</div>

<p class="more-link">
  <a href="/projects/">View all projects →</a>
</p>