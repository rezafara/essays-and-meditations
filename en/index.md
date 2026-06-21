---
layout: default
title: English Essays
permalink: /en/
---

# English Essays

{% assign essays = site.essays_en | sort: "date" | reverse %}
{% if essays.size > 0 %}
{% for essay in essays %}
- [{{ essay.title }}]({{ essay.url }})
{% endfor %}
{% else %}
No essays yet.
{% endif %}
