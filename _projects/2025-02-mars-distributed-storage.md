---
layout: single
title: "Mars Distributed Storage System"
collection: projects
permalink: /projects/mars-ds/
date: 2025-02-01
venue: "Distributed Systems (2024-2025)"
excerpt: "Peer-to-peer, fault-tolerant key-value store in Java (Akka Actors): consistent hashing, 2PC, quorum replication, crash/recovery."
repo: https://github.com/antodila/mars-distributed-storage-system
---

Proof-of-concept of a **peer-to-peer**, fault-tolerant, highly available key-value store built in **Java (Akka Actors)**.  
Implements **consistent hashing**, **Two-Phase Commit (2PC)** for atomic writes, and **quorum-based replication (R + W > N)** to guarantee sequential consistency.  
Includes **node crash/recovery simulation**, **data handoff**, and **read-repair**.


{% if page.repo %}
<p><a class="btn btn--primary btn--small" href="{{ page.repo }}" target="_blank" rel="noopener">GitHub Repo</a></p>
{% endif %}

<p><a class="btn btn--light-outline btn--small" href="{{ '/projects/' | relative_url }}">← Back to Projects</a></p>
