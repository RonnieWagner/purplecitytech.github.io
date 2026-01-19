---
layout: default
title: Builds
permalink: /builds.html
---

## Current & Past Builds

<div class="build-grid">
{% for build in site.builds %}
  <div class="build-card">
    <h3>{{ build.title }}</h3>

    <p>
      <span class="status {{ build.status }}">{{ build.status }}</span><br>
      <strong>Price:</strong> {{ build.price }}
    </p>

    <a href="{{ build.url }}">View build details →</a>
  </div>
{% endfor %}
</div>

