---
layout: single
title: "Mars Distributed Storage System"
collection: projects
permalink: /projects/mars-ds/
date: 2025-02-01
venue: "Distributed Systems (2024-2025)"
excerpt: "Peer-to-peer, fault-tolerant key-value store in Java (Akka Actors): consistent hashing, 2PC, quorum replication, crash/recovery."
# Se vuoi che il titolo sulla lista punti diretto alla repo, decommenta la riga sotto
# link: https://github.com/antodila/mars-distributed-storage-system
# Bottoni nella pagina (opzionali)
repo: [https://github.com/antodila/mars-distributed-storage-system](https://github.com/antodila/distributed-systems-project)
---

Proof-of-concept of a **peer-to-peer**, fault-tolerant, highly available key-value store built in **Java (Akka Actors)**.  
Implements **consistent hashing**, **Two-Phase Commit (2PC)** for atomic writes, and **quorum-based replication (R + W > N)** to guarantee sequential consistency.  
Includes **node crash/recovery simulation**, **data handoff**, and **read-repair**.


<p><a class="btn btn--light-outline btn--small" href="{{ '/projects/' | relative_url }}">← Back to Projects</a></p>
