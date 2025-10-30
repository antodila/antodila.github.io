---
layout: archive
title: "Projects"
permalink: /projects/
author_profile: true
---

{% assign items = site.projects | sort: 'date' | reverse %}
{% for post in items %}
  {% include archive-single.html %}
{% endfor %}
