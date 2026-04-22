---
layout: default
title: Projects
description: Selected repositories, tools, userscripts, and experiments by Rait Nigol.
permalink: /projects/
---

<p class="page-intro">
  A broader list of projects, tools, userscripts, and experiments.
</p>

{% assign categories = site.data.repos | map: "category" | uniq | sort %}

{% for category in categories %}
  <section class="project-section">
    <h2 class="category-heading">{{ category | capitalize }}</h2>

    <div class="repo-grid">
      {% assign repos = site.data.repos | where: "category", category | sort: "priority" %}
      {% for repo in repos %}
        <article class="repo-card">
          <h3 class="repo-title">
            <a href="{{ repo.url }}" target="_blank" rel="noopener noreferrer">{{ repo.name }}</a>
          </h3>

          <p class="repo-description">{{ repo.description }}</p>
          <p class="repo-link-row">
            <a class="repo-link" href="{{ repo.url }}" target="_blank" rel="noopener noreferrer">Open project →</a>
          </p>

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
  </section>
{% endfor %}