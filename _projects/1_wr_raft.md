---
layout: page
title: "WR-Raft"
importance: 1
status: "Paper in preparation"
stack: [Raft, Consensus, Replication, Storage]
size: lead
---

A Raft variant that weights quorum participation by each follower's observed fsync latency, tracked as an exponentially weighted moving average. The work includes an analysis against Cabinet (VLDB &rsquo;25) and WOC and documents the correctness hazards of weighted quorums. I mentor three interns on the project.
