---
layout: single
title: "Impact of Aggressive Quantization on Deepfake Detection"
collection: projects
permalink: /projects/deepfake-quantization/
date: 2026-01-14
venue: "Multimedia Data Security (2025-2026)"
excerpt: "Comprehensive study on how 4-bit quantization (FP4) in SOTA diffusion models (SD3, Flux.1) acts as an adversarial attack against forensic detectors."
header:
  teaser: /images/plot_heatmap_summary.png
  overlay_image: /images/deepfake_header.png
  overlay_filter: 0.5
---

A research project analyzing the **trade-off between efficiency and security** in modern Generative AI.
As the industry moves towards **Edge AI** by compressing models to **4-bit (FP4)**, this study investigates whether this aggressive quantization unintentionally erases the forensic "fingerprints" required for deepfake detection.

### 🔬 Experimental Setup
I developed an automated pipeline using **Python**, **PyTorch**, and **Diffusers** to generate and analyze a massive dataset:
* **Dataset:** **10,500 images** generated across 6 architectures (Legacy `SD1.5`, High-Res `SDXL`, and SOTA Transformers `SD3`, `Flux.1`).
* **Quantization:** Each architecture was tested at 4 precision levels: `FP32`, `FP16`, `FP8`, and `FP4`.
* **Detectors:** Benchmarked 4 distinct detectors, comparing **End-to-End** trainable models (e.g., *NPR*) vs. **Feature-Based** frozen backbones (e.g., *CLIP-D*).

### 🚀 Key Findings
The analysis revealed a critical vulnerability in the current generation of forensic tools:
1.  **The "SD3 Anomaly":** While Stable Diffusion 3 represents the State-of-the-Art, its **FP4 quantized version** becomes practically invisible to noise-based detectors (End-to-End), causing accuracy to plummet from **~99% to ~27%**.
2.  **Robustness of Feature-Based Detectors:** Detectors relying on semantic anomalies (like *CLIP-D*) proved to be "compression-agnostic," maintaining high detection rates even on heavily compressed images.
3.  **Flux.1 Resilience:** Unlike SD3, the *Flux.1* model generates structural artifacts strong enough to survive 4-bit quantization, remaining detectable.

### 📊 Visual Evidence
The study utilized Kernel Density Estimation (KDE) plots to visualize the distribution shift caused by quantization.

<figure style="text-align: center; margin: 20px 0;">
  <img src="/images/plot_kde_CLIP-D.png" alt="KDE Plot showing distribution shift" style="max-width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
  <figcaption style="font-size: 0.9em; color: #666; margin-top: 5px;">
    Figure 1: The "Distribution Shift". The yellow curve (FP4) shifts left compared to the purple baseline (FP32), indicating that the detector fails to distinguish fake images from real ones under aggressive quantization.
  </figcaption>
</figure>

This work suggests that as Edge AI becomes standard, future detectors must include quantized samples in their training data to ensure security.

<div style="display: flex; gap: 10px; margin-top: 30px; margin-bottom: 30px;">
  <a href="[#](https://github.com/antodila/quantization-deepfake-detection)" class="btn btn--primary">
    <i class="fab fa-github"></i> View Source Code
  </a>
  
  <a href="/files/MDS_Final_Presentation.pdf" class="btn btn--info">
    <i class="fas fa-file-pdf"></i> View Presentation
  </a>
</div>

<p><a class="btn btn--light-outline btn--small" href="{{ '/projects/' | relative_url }}">← Back to Projects</a></p>
