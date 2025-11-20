---
layout: single
title: "Sviluppo di un Digital Twin per l'analisi di copertura wireless in ambienti urbani"
collection: projects
permalink: /projects/bachelor-thesis/
date: 2024-09-26
venue: "Bachelor's Thesis, University of Trento (2023-2024)"
excerpt: "Design and implementation of a robust Client-Server architecture (Android/Java & Python) for reliable voice message transmission over TCP sockets in critical scenarios."
# repo: https://github.com/antodila/your-repo-if-it-exists
---

**Abstract:**
This thesis addresses the design and development of a voice communication system dedicated to the military sector, where network stability and strict data flow control are critical requirements.

The project implements a complete **Client-Server** architecture:
* **Mobile Client (Android/Java):** A custom application handling raw audio acquisition (`MediaRecorder`), encoding, and data packet transmission.
* **Central Server (Python):** A backend engine built on **TCP Sockets** and **Multithreading** to handle concurrent connections, ensuring the reliable reception and routing of voice messages among field operators.

The work analyzes the challenges of real-time communication over IP networks, transmission buffer management, and the design of a custom application-layer protocol for secure message exchange.

{% if page.repo %}
<p><a class="btn btn--light-outline btn--small" href="{{ page.repo }}" target="_blank" rel="noopener">GitHub Repo</a></p>
{% endif %}

<p><a class="btn btn--primary btn--small" href="https://antodila.github.io/files/DiLauro_Antonio_laurea_2023-2024.pdf" target="_blank" rel="noopener">Download Thesis (PDF)</a></p>

<p><a class="btn btn--light-outline btn--small" href="{{ '/projects/' | relative_url }}">← Back to Projects</a></p>
