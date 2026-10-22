---
layout: post
title: "Waiting for QUIC: Passive Measurements to Understand QUIC Deployments"
date: 2026-10-19
paper_authors: "J. Mücke, M. Nawrocki, R. Hiesgen, P. Sattler, J. Zirngibl, G. Carle, J. Luxemburk, T. C. Schmidt, M. Wählisch"
paper_venue: "ACM CoNEXT 2025"
paper_url: "https://dl.acm.org/doi/pdf/10.1145/3768988"
week: 4
tags: [quic, passive-measurement, network-telemetry, internet-infrastructure]
---

## Key Idea

The key problem is that the internal QUIC configurations of large internet providers are often hidden, which makes it difficult to understand how QUIC is deployed under the hood. The paper's core contribution is a passive measurement methodology using backscatter traffic from UCSD network telescope to infer QUIC deployment characteristics, including retransmission behavior, load-balancer configurations, and infrastructure changes over time.

## Critique

The paper convincingly demonstrates that passive measurements can reveal meaningful information about large-scale QUIC deployments without requiring direct access to providers' infrastructure. However, its methodology relies on backscatter traffic, which means it may not accurately represent normal QUIC connections, and its ability to infer internal configurations depends on observable packet characteristics that providers can change over time.

## Connections

This paper connects to Baltra and Misa's paper because all three use empirical measuremeents to uncover underlying Internet behavior that is hard to observe directly. This paper uses passive QUIC measurements to infer hidden deployment configurations, much like Balta's paper that uses vantage points to identify partial connectivity, demonstrating how external observations can reveal underlying Internet infrastructure.
