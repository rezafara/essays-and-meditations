---
layout: default
title: مقاله‌های فارسی
permalink: /fa/
lang: fa
text_direction: rtl
---

{% assign essays = site.essays_fa | sort: "date" | reverse %}

<section class="blog-index">
  <p class="eyebrow">فارسی</p>
  <h1>مقاله‌ها</h1>

  {% if essays.size > 0 %}
  <ol class="essay-list">
    {% for essay in essays %}
    <li>
      <a href="{{ essay.url | relative_url }}">{{ essay.title }}</a>
      {% if essay.date %}
      <time datetime="{{ essay.date | date_to_xmlschema }}">{{ essay.date | date: "%Y-%m-%d" }}</time>
      {% endif %}
    </li>
    {% endfor %}
  </ol>
  {% else %}
  <p>هنوز مقاله‌ای منتشر نشده است.</p>
  {% endif %}
</section>
