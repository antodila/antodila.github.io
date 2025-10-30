---
title: "Mars Distributed Storage System"
collection: projects
permalink: /projects/mars-ds/
date: 2025-02-01
venue: "Distributed Systems (2024–2025)"
excerpt: "Peer-to-peer fault-tolerant key–value store with Akka Actors in Java; consistent hashing, 2PC, quorums, read-repair."
links:
  - name: Link available on request
    url: "#"
---

Proof-of-concept of a peer-to-peer, fault-tolerant, highly available key-value store in **Java (Akka Actors)**.  
Key points: consistent hashing, **Two-Phase Commit (2PC)** for atomic writes, quorum-based replication (R+W>N), read-repair, crash/recovery simulation and data handoff.
