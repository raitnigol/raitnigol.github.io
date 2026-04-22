---
layout: page
title: Rait Nigol
permalink: /
---

<div class="home-intro">
  <p class="home-lead">
    Personal hub for projects, tools, experiments, and other things I build.
  </p>

  <div class="home-links">
    <a class="button-link" href="https://github.com/raitnigol">GitHub</a>
  </div>
</div>

## Featured repositories

<div class="repo-grid">
  {% assign repos = site.data.repos | where: "featured", true | sort: "priority" %}
  {% for repo in repos %}
    <article class="repo-card">
      <div class="repo-card-header">
        <h3 class="repo-title">
          <a href="{{ repo.url }}">{{ repo.name }}</a>
        </h3>

        {% if repo.status %}
          <span class="repo-status repo-status-{{ repo.status | slugify }}">{{ repo.status }}</span>
        {% endif %}
      </div>

      <p class="repo-description">{{ repo.description }}</p>

      {% if repo.tags %}
        <div class="repo-tags">
          {% for tag in repo.tags %}
            <span class="tag tag-{{ tag | slugify }}">{{ tag }}</span>
          {% endfor %}
        </div>
      {% endif %}

      {% if repo.tech %}
        <div class="repo-tech">
          {% for item in repo.tech %}
            <span class="tech-pill">{{ item }}</span>
          {% endfor %}
        </div>
      {% endif %}
    </article>
  {% endfor %}
</div>
