---
layout: archive
title: "Teaching"
permalink: /teaching/
author_profile: true
---

{% include base_path %}

Below is a selection of my recent teaching, tutoring, and workshop experience.

---

{% for course in site.data.teaching %}
<div class="teaching-card">

  <h3 class="teach-title">
    <a href="{{ course.link }}" target="_blank">{{ course.title }}</a>
  </h3>

  <p class="teach-meta">
    <strong>{{ course.role }}</strong> — {{ course.institution }} ({{ course.year }})
  </p>

  <p class="teach-desc">{{ course.description }}</p>

</div>
---
{% endfor %}
