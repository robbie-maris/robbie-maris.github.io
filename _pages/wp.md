---
layout: archive
title: "Working papers"
permalink: /wp/
author_profile: true
---

{% include base_path %}

Below are a selection of my recent and forthcoming publications, grouped by research area.  
Click on each title to expand the abstract and view a related figure.

---

{% for group in site.data.wp %}
## {{ group.theme }}
{% for pub in group.publications %}
<div class="publication-card">

  <h3 class="pub-title">
    <a href="{{ pub.link }}" target="_blank">{{ pub.title }}</a>
  </h3>

  <p class="pub-meta">
    <strong>{{ pub.authors }}</strong> ({{ pub.year }}).<br>
    <em>{{ pub.journal }}</em>.
  </p>

  <details>
    <summary><strong>View abstract & figure</strong></summary>
    <p>{{ pub.abstract }}</p>
    {% if pub.image %}
    <p><img src="{{ pub.image }}" alt="{{ pub.title }}" class="pub-figure"></p>
    {% endif %}
  </details>

</div>

---
{% endfor %}
{% endfor %}
