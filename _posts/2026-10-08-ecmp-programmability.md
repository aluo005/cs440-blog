---
layout: post
title: "Unlocking ECMP Programmability for Precise Traffic Control"
date: 2026-10-08
paper_authors: "Y. Liu, Y. Xiao, X. Zhang, W. Dang, H. Liu, X. Li, Z. He, J. Wang, A. Kuzmanovic, A. Chen, C. Miao"
paper_venue: "USENIX NSDI 2025"
paper_url: "https://www.usenix.org/system/files/nsdi25-liu-yadong.pdf"
week: 3
tags: [ecmp, traffic-engineering, data-center-networks, routing]
---

## Key Idea

The key problem is that traditional ECMP uses hashing to assign flows to equal-cost paths, which introduces randomness. This makes it difficult to precisely control the path of an individual flow. P-ECMP's core contribution is using multiple existing ECMP groups and a packet selector to enable applications to deliberately select alternative paths without randomness, while preserving normal ECMP behavior for regular traffic.

## Critique

The paper convincingly demonstrates that PTC can be implemented without redesigning hardware, but rather exploiting existing features. It demonstrated the feasibility via production deployment at Tencent, showing significant results in reduction of network failure downtime. However, a limitation is that P-ECMP requires alternative paths to exist and cannot detect network failures, which can hinder its effectiveness.

## Connections

This paper connects specifically with Raha since both address weaknesses in how networks handle failures. Raha can potentially complement P-ECMP very well, as Raha detects network degradations, enabling P-ECMP to change selectors to send flows over different paths.

