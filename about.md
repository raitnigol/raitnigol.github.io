---
layout: default
title: About
description: About Rait Nigol and the focus of this site.
permalink: /about/
---

<p class="page-intro">
  This site is a small hub for selected work from <a href="https://github.com/raitnigol" target="_blank" rel="noopener noreferrer">github.com/raitnigol</a>.
</p>

<div class="content-block">
  <p>
    Most of the projects here revolve around tooling, automation, userscripts, scraping, small utilities, and experiments that solve practical problems or explore ideas quickly.
  </p>

  <p>
    The goal is not to mirror every repository, but to keep a curated, readable front page for the projects that are actually worth surfacing.
  </p>

  <p>
    Elsewhere:
  </p>

  <ul class="clean-list">
    {% for social in site.data.socials %}
      <li><a href="{{ social.url }}" target="_blank" rel="noopener noreferrer">{{ social.name }}</a></li>
    {% endfor %}
  </ul>
</div>