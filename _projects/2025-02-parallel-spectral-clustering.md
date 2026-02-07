---
layout: single
title: "Extreme-Scale Spectral Clustering (Hybrid MPI + OpenMP)"
collection: projects
permalink: /projects/mpi-spectral-clustering/
date: 2026-02-07
venue: "High Performance Computing (2026)"
excerpt: "A distributed HPC engine capable of clustering 2 million points. Features Nyström Approximation, Cache Blocking, and Self-Tuning Kernels for biological data analysis."
header:
  teaser: /images/spectral_clustering_result.png
  overlay_image: /images/spectral_clustering_result.png
  overlay_filter: 0.5
---

A high-performance implementation of the **Spectral Clustering** algorithm designed for distributed HPC environments.

This project overcomes the traditional **Memory Wall** (O(N²)) and **Compute Wall** (O(N³)) of spectral methods. By transitioning from a standard exact solver to a **Distributed Nyström Approximation**, the system scales from small biological datasets to massive synthetic benchmarks (**2,000,000 points**) on standard cluster hardware.

### 🚀 Key Technical Highlights

**Hybrid Parallel Architecture:**
* **Inter-Node (MPI):** Handles coarse-grained tasks like data distribution (Row-Block layout) and global synchronization (Landmark selection).
* **Intra-Node (OpenMP):** Maximizes core utilization with multi-threading for distance calculations and matrix operations.

**Algorithmic Optimizations:**
* **Distributed Nyström Approximation:** Reduces spectral complexity from O(N³) to O(S³) by computing affinity against a subset of global landmarks (S << N).
* **Zero-Network Projection:** Local calculation of spectral embeddings (`U_local = W_local × U_S Λ_S⁻½`) eliminating expensive collective communication.
* **Single-Pass Distributed K-Means:** Optimized convergence strategy leveraging the high separability of the spectral embedding.

**Hardware-Aware Design:**
* **Cache Blocking (Tiling):** Matrix operations are tiled (block size 64) to fit in L1/L2 cache, minimizing latency.
* **SIMD Vectorization:** Data layout ensures efficient use of CPU vector units for Euclidean distance kernels.

### 🧬 Biological Validation & Scaling

The system was designed with a dual-mode engine to balance **Topological Precision** and **Extreme Scalability**:

* **Quality Mode (Exact Kernel):** Validated on the **Mouse Cell Atlas (MCA)** dataset (~20k single cells). Used **Self-Tuning Kernels** (Zelnik-Manor & Perona) to correctly identify non-convex biological manifolds (tissues) despite multi-scale densities.
* **Throughput Mode (Nyström):** Benchmarked on the **University of Trento HPC Cluster**, achieving linear scaling up to **2,000,000 points**, effectively breaking the 32 TB memory requirement of the naive approach.

### 📊 Visual Results

<figure style="text-align: center; margin: 20px 0;">
  <img src="/images/spectral_clustering_result.png" alt="Spectral Clustering Results" style="max-width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
  <figcaption style="font-size: 0.9em; color: #666; margin-top: 5px;">
    Figure 1: Topological recovery of non-convex structures (spirals, circles) on the adversarial benchmark dataset.
  </figcaption>
</figure>

<div style="display: flex; gap: 10px; margin-top: 30px; margin-bottom: 30px;">
  <a href="https://github.com/SincereJuliya/HPC" class="btn btn--primary">
    <i class="fab fa-github"></i> View Source Code
  </a>
  
  <a href="/files/HPC_Report_Spectral_Clustering.pdf" class="btn btn--info">
    <i class="fas fa-file-pdf"></i> Read Full Report
  </a>
</div>

<p><a class="btn btn--light-outline btn--small" href="{{ '/projects/' | relative_url }}">← Back to Projects</a></p>
