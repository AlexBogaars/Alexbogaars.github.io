---
layout: archive
title: "Macroeconomic notes"
permalink: /macro-notes/
author_profile: true
---

{% include base_path %}

{% for post in site.macro_notes reversed %}
  {% include archive-single.html %}
{% endfor %}
