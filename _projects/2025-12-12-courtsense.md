---
layout: single
title: "Automated Basketball Tactical Analysis (CourtSense)"
collection: projects
permalink: /projects/courtsense/
date: 2025-12-08
venue: "Sport Tech (2025-2026)"
excerpt: "Interactive tactical dashboard for basketball analysis: Space Ownership (Voronoi), player workload tracking, and hybrid 2D metric estimation using Computer Vision."
repo: https://github.com/antodila/CourtSense
---

Development of a **computer vision-based tactical dashboard** for basketball analytics, built with **Python (Streamlit, OpenCV, Pandas, SciPy)**.  
The system processes tracking data to generate advanced metrics such as **Space Ownership** (via Voronoi Tessellation), **Team Compactness** (Convex Hull), and dynamic **Off-Ball Movement analysis**.  
Features a novel **"Hybrid Tracking" engine** that combines pixel-perfect bounding box collision detection for robust **ball possession logic** (filtering "fly-by" errors) with estimated metric conversion for real-world **speed and workload analysis**. Includes a dual-view interface with synchronized video playback and a live **2D tactical radar**.

<p>
  {% if page.repo %}
    <a class="btn btn--primary btn--small" href="{{ page.repo }}" target="_blank" rel="noopener">GitHub Repo</a>
  {% endif %}
  
  <a class="btn btn--primary btn--small" href="https://courtsense.streamlit.app/" target="_blank" rel="noopener">Live Demo (App)</a>
</p>

<p><a class="btn btn--light-outline btn--small" href="{{ '/projects/' | relative_url }}">← Back to Projects</a></p>
