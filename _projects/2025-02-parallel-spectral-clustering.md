---
layout: single
title: "Hybrid Parallel Spectral Clustering (MPI + OpenMP)"
collection: projects
permalink: /projects/mpi-spectral-clustering/
date: 2026-01-30
venue: "High Performance Computing (2026)"
excerpt: "High-performance implementation using Hybrid MPI+OpenMP; Self-Tuning Kernel, distributed matrix construction, and scaling on biological datasets."
header:
  teaser: /assets/images/spectral_clustering_result.png
  overlay_image: /assets/images/spectral_clustering_result.png
  overlay_filter: 0.5 # Scurisce leggermente l'immagine per leggere meglio il titolo
---

A high-performance implementation of the **Spectral Clustering** algorithm designed for distributed HPC environments.
This project addresses the computational bottlenecks of clustering large-scale datasets (the $O(N^2)$ memory and $O(N^3)$ compute complexity) by adopting a **Hybrid Parallel Architecture**.

### 🚀 Key Features
* **Hybrid Parallelism:** Combines **MPI** for distributed memory communication across nodes and **OpenMP** for shared memory multithreading within nodes.
* **Self-Tuning Kernel:** Implements the *Zelnik-Manor & Perona* adaptive scaling to correctly cluster multi-density datasets.
* **Optimized Memory:** Efficient row-based decomposition to distribute the Similarity Matrix construction load.
* **Real-World Application:** Validated on synthetic benchmarks and scaled to the **Mouse Cell Atlas (MCA)** biological dataset (~20k single cells).

### 📊 Visual Results & Performance
The algorithm successfully identifies non-convex clusters (spirals, circles) that standard K-Means fails to separate.

<figure style="text-align: center; margin: 20px 0;">
  <img src="/images/spectral_clustering_result.png" alt="Spectral Clustering Results" style="max-width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
  <figcaption style="font-size: 0.9em; color: #666; margin-top: 5px;">
    Figure 1: Clustering results on the synthetic benchmark dataset (N=7,500).
  </figcaption>
</figure>

Tested on the **University of Trento HPC cluster**, the solution demonstrates strong scalability and significant speedup compared to the sequential implementation.

<div style="display: flex; gap: 10px; margin-top: 30px; margin-bottom: 30px;">
  <a href="https://github.com/SincereJuliya/HPC" class="btn btn--primary">
    <i class="fab fa-github"></i> View Source Code
  </a>
  
  <a href="/files/HPC_Report_Spectral_Clustering.pdf" class="btn btn--info">
    <i class="fas fa-file-pdf"></i> Read Full Report
  </a>
</div>

<p><a class="btn btn--light-outline btn--small" href="{{ '/projects/' | relative_url }}">← Back to Projects</a></p>
