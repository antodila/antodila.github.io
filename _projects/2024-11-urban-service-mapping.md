---
layout: single
title: "Urban Service Mapping WebApp"
collection: projects
permalink: /projects/urban-service-mapping/
date: 2024-11-20
venue: "Software Engineering (2024)"
excerpt: "Full-stack web application for real-time reporting of urban issues; Node.js/Express, React, MongoDB; cloud deploy."
repo: "#"   # puoi sostituire con il link GitHub effettivo
demo: https://ing-software-group14.onrender.com
---

Full-stack webapp for reporting and monitoring urban infrastructure issues in real time.  
Stack: **Node.js/Express**, **React**, **MongoDB**; cloud deployment on Render.  
Roles: user reporting, admin management, live status and alternative path suggestions.

{% if page.repo or page.demo %}
<div class="btn-links">
  {% if page.repo %}
  <a class="btn btn--primary btn--small" href="{{ page.repo }}" target="_blank" rel="noopener">GitHub Repo</a>
  {% endif %}
  {% if page.demo %}
  <a class="btn btn--small" href="{{ page.demo }}" target="_blank" rel="noopener">Live Demo</a>
  {% endif %}
</div>
{% endif %}

<p><a class="btn btn--light-outline btn--small" href="{{ '/projects/' | relative_url }}">← Back to Projects</a></p>
