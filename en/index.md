---
layout: default
title: English Essays
permalink: /en/
lang: en
text_direction: ltr
---

{% assign essays = site.essays_en | sort: "date" | reverse %}

<section class="blog-index">
  <p class="eyebrow">English</p>
  <h1>Essays</h1>

  {% if essays.size > 0 %}
  <ol class="essay-list">
    {% for essay in essays %}
    <li>
      <a href="{{ essay.url | relative_url }}">{{ essay.title }}</a>
      {% if essay.date %}
      <time datetime="{{ essay.date | date_to_xmlschema }}">{{ essay.date | date: "%B %-d, %Y" }}</time>
      {% endif %}
    </li>
    {% endfor %}
  </ol>
  {% else %}
  <p>No essays yet.</p>
  {% endif %}
</section>
