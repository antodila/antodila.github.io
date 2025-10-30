---
layout: archive
title: "Projects"
permalink: /projects/
author_profile: true
---

{% include base_path %}

A selection of academic and technical projects.

{% for post in site.projects reversed %}
  {% include archive-single.html %}
{% endfor %}
