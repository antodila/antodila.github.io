---
layout: single
title: "Robust Digital Watermarking System (Shadowmark)"
collection: projects
permalink: /projects/shadowmark/
date: 2025-11-05
venue: "Multimedia Data Security (2025-2026)"
excerpt: "Robust spread-spectrum watermarking system (DCT domain) in Python: adaptive embedding, ROC-based thresholding, and automated attack resilience testing."
repo: https://github.com/antodila/multimedia_data_security
---

Implementation of a **robust spread-spectrum watermarking** system operating in the **DCT domain**, developed in **Python (NumPy, SciPy, OpenCV)**.  
Features an **adaptive embedding strength** based on local image properties (Weber's Law) and a novel **"Feature Centering" detection logic** that achieved **0.00% False Positive Rate** during validation.  
Includes a complete pipeline for **ROC curve analysis** to determine optimal detection thresholds and an automated suite for testing resilience against **JPEG compression**, **noise**, and **geometric attacks**.

{% if page.repo %}
<p><a class="btn btn--primary btn--small" href="{{ page.repo }}" target="_blank" rel="noopener">GitHub Repo</a></p>
{% endif %}

<p><a class="btn btn--light-outline btn--small" href="{{ '/projects/' | relative_url }}">← Back to Projects</a></p>
