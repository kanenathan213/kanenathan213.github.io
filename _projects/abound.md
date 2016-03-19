---
layout: project
project_id: abound
---
{% assign steps = site.data.projects[page.project_id].steps %}

{% for step in steps %}
<div>
  {{ step.caption_title }}
  {{ step.caption }}
</div>
{% endfor %}
