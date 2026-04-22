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
### [{{ repo.name }}]({{ repo.url }})

{{ repo.description }}

{% if repo.tags %}
Tags: {{ repo.tags | join: ", " }}
{% endif %}

{% endfor %}
