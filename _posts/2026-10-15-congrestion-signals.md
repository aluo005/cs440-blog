---
layout: post
title: "No Signal to Rule Them All: A Systematic Analysis of In-Network Congestion Signals"
date: 2026-10-14
paper_authors: "S. McClure, N. Dukkipati, S. Ratnasamy, S. Shenker"
paper_venue: "NINeS 2026"
paper_url: "https://2026.nines-conference.org/papers/p012-McClure.pdf"
week: 4
tags: [congestion-control, in-network-telemetry, networking, performance]
---

## Key Idea

The key problem is to determine if additional in-network congestion signals actually improve congrestion control compared to traditional end-to-end measurements. The paper's contribution is a systemic evaluation framework by using learned congestion control algorithms to compare different signals, finding that in-network telemetry provides less than 3% average performance improvement over modern signals.

## Critique

The paper convincingly challenges the assumption that more detailed network information will definitively improve congestion control, demonstrating modern end-to-end signals can achieve comparable performance. However, the caveat is that the evaluation primarily relies on simulations and learned algortihms through limited set of network conditions, meaning results may not be fully generalized to real-world networks that may have more complex traffic patterns.

## Connections

This paper connects to P-ECMP as both improve network performance and reliability. This paper investigates whether additional network information improves congestion control, finding that traditional end-to-end signals solid performance as well, much like P-ECMP exploiting existing hardware for performance improvement.

