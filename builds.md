---
layout: default
title: Builds
permalink: /builds.html
---

## Current & Past Builds

<div class="build-grid">
{% for build in site.builds %}
  <div class="build-card {{ build.status | downcase }}">
    <h3>{{ build.title }}</h3>

    <p class="build-status status-{{ build.status | downcase }}">
      {{ build.status }}
    </p>

    <ul class="build-specs">
      {% if build.cpu %}<li><strong>CPU:</strong> {{ build.cpu }}</li>{% endif %}
      {% if build.gpu %}<li><strong>GPU:</strong> {{ build.gpu }}</li>{% endif %}
      {% if build.ram %}<li><strong>RAM:</strong> {{ build.ram }}</li>{% endif %}
      {% if build.storage %}<li><strong>Storage:</strong> {{ build.storage }}</li>{% endif %}
    </ul>

    {% if build.price %}
      <p class="build-price">{{ build.price }}</p>
    {% endif %}

    <a class="build-link" href="{{ build.url | relative_url }}">
      View build →
    </a>
  </div>
{% endfor %}
</div>

