---
layout: default
title: مقاله‌های فارسی
permalink: /fa/
---

<div dir="rtl" lang="fa">

# مقاله‌های فارسی

{% assign essays = site.essays_fa | sort: "date" | reverse %}
{% if essays.size > 0 %}
{% for essay in essays %}
- [{{ essay.title }}]({{ essay.url }})
{% endfor %}
{% else %}
هنوز مقاله‌ای منتشر نشده است.
{% endif %}

</div>
