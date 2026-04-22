---
layout: home
title: Home
permalink: /
---

# Rait Nigol

GitHub, projects, links, and other things.

- [GitHub](https://github.com/raitnigol)

## Featured repositories

{% for repo in site.data.repos %}
  <article class="repo-card">
    <h3><a href="{{ repo.url }}">{{ repo.name }}</a></h3>
    <p>{{ repo.description }}</p>

    {% if repo.tags %}
      <div class="repo-tags">
        {% for tag in repo.tags %}
          <span class="tag tag-{{ tag | slugify }}">{{ tag }}</span>
        {% endfor %}
      </div>
    {% endif %}
  </article>
{% endfor %}
