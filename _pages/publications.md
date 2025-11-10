---
layout: archive
title: "Selected Publications"
permalink: /publications/
author_profile: true
---

{% include base_path %}

Below are a selection of my recent and forthcoming publications, grouped by research area.  
Click on each title to expand the abstract and view a related figure.

---

{% for group in site.data.publications %}
## {{ group.theme }}
{% for pub in group.publications %}
<div class="publication">

### [{{ pub.title }}]({{ pub.link }})
**{{ pub.authors }}**. *{{ pub.journal }}.*

<details>
  <summary><strong>View abstract & figure</strong></summary>
  <p>{{ pub.abstract }}</p>
  {% if pub.image %}
  <p><img src="{{ pub.image }}" alt="{{ pub.title }}" style="max-width:500px; border-radius:8px; margin-top:10px;"></p>
  {% endif %}
</details>

</div>
---
{% endfor %}
{% endfor %}
