---
layout: single
title: "Digital Twin for Wireless Coverage Analysis"
collection: projects
permalink: /projects/bachelor-thesis/
date: 2024-09-26
venue: "Bachelor's Thesis, University of Trento (2023-2024)"
excerpt: "Development of a Digital Twin to simulate urban wireless coverage using Blender, Mitsuba, and Nvidia Sionna (Ray Tracing)."
# repo: https://github.com/antodila/your-repo-if-exists
---

**Abstract:**
This thesis focuses on the development of a **Digital Twin** to simulate and analyze wireless signal propagation in complex urban environments. The project bridges 3D modeling and physical layer simulation to create accurate coverage maps.

Key Technologies & Methodologies:
* **Nvidia Sionna:** Utilized this GPU-accelerated library for physical layer (PHY) simulation and **Ray Tracing** to model radio wave propagation.
* **Blender & Mitsuba:** Employed for 3D modeling of urban scenes and rendering, creating a high-fidelity digital replica of the target environment.
* **Python & TensorFlow:** Used for scripting the simulation pipeline, processing data, and generating coverage metrics (e.g., heatmaps, SNR analysis).

{% if page.repo %}
<p><a class="btn btn--light-outline btn--small" href="{{ page.repo }}" target="_blank" rel="noopener">GitHub Repo</a></p>
{% endif %}

<p><a class="btn btn--primary btn--small" href="https://antodila.github.io/files/DiLauro_Antonio_laurea_2023-2024.pdf" target="_blank" rel="noopener">Download Thesis (PDF)</a></p>

<p><a class="btn btn--light-outline btn--small" href="{{ '/projects/' | relative_url }}">← Back to Projects</a></p>
