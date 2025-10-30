---
title: "Mars Distributed Storage System"
collection: projects
permalink: /projects/mars-ds/
date: 2025-02-01
venue: "Distributed Systems (2024–2025)"
excerpt: "Peer-to-peer fault-tolerant key–value store with Akka Actors in Java; consistent hashing, 2PC, quorums, read-repair."
# Header opzionale (metti un'immagine se ce l'hai in /images/projects/)
header:
  overlay_color: "#000"
  overlay_filter: "0.35"
  image: /images/projects/mars-ds-hero.jpg
# Link esterni utili
repo: https://github.com/antodila/<repo-se-pubblico-o-copia>
demo:
links:
  - name: Link available on request
    url: "#"
---

Proof-of-concept of a peer-to-peer, fault-tolerant, highly available key-value store in **Java (Akka Actors)**.  
Key points: consistent hashing, **Two-Phase Commit (2PC)** for atomic writes, quorum-based replication (**R + W > N**), read-repair, crash/recovery simulation and data handoff.

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

<a class="btn btn--light-outline btn--small" href="{{ '/projects/' | relative_url }}">← Back to Projects</a>
