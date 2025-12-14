---
layout: single
title: "Automated Basketball Tactical Analysis (CourtSense)"
collection: projects
permalink: /projects/courtsense/
date: 2025-12-14
venue: "Sport Tech (2025-2026)"
excerpt: "Advanced tactical dashboard featuring Automated Game Phase Recognition, dynamic physiological profiling, and Space Ownership (Voronoi) analysis."
repo: https://github.com/antodila/CourtSense
---

Development of a **computer vision-based tactical dashboard** for basketball analytics, built with **Python (Streamlit, OpenCV, Pandas, SciPy)**.

The system features a **Tactical Intelligence Engine** that automatically segments gameplay into **Offense vs. Defense phases** based on possession flow, allowing for context-aware metric filtering.
Advanced signal processing (Savitzky-Golay filters) is used for **physiological profiling**, providing realistic **Dynamic Speed Analysis** (Walk/Jog/Sprint detection) and workload tracking.

Key features include:
* **Space Ownership:** Real-time Voronoi Tessellation and Convex Hull for team compactness.
* **Context-Aware Analytics:** Interactive timeline to filter metrics by specific game phases.
* **Hybrid Tracking Engine:** Combines pixel-perfect collision detection for robust ball possession logic with homography transformation for 2D metric estimation.

<p>
  {% if page.repo %}
    <a class="btn btn--primary btn--small" href="{{ page.repo }}" target="_blank" rel="noopener">GitHub Repo</a>
  {% endif %}
  
  <a class="btn btn--primary btn--small" href="https://courtsense.streamlit.app/" target="_blank" rel="noopener">Live Demo (App)</a>
</p>

<p><a class="btn btn--light-outline btn--small" href="{{ '/projects/' | relative_url }}">← Back to Projects</a></p>
