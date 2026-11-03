---
layout: post
title: "Exploring the Benefits of Carbon-Aware Routing"
date: 2026-11-02
paper_authors: "S. El-Zahr, P. Gunning, N. Zilberman"
paper_venue: "ACM CoNEXT 2023"
paper_url: "https://dl.acm.org/doi/pdf/10.1145/3629165"
week: 6
tags: [carbon-aware-routing, sustainability, traffic-engineering, energy-efficiency, networking]
---

## Key Idea

The key problem is that traditional routing algorithms prioritize metrics such as latency and bandwidth without much consideration on the environment, such as carbon emissions that came from network traffic. The paper's core contribution is CATE, a carbon-aware traffic engineering algorithm that considers regional carbon intensity and routers' dynamic power consumption when selecting network paths, while allowing unused ports to power down to reduce overall carbon emissions.

## Critique

The paper convincingly demonstrates that incorporating carbon-related metrics into routing decisions can reduce network emissions without requiring modifications to existing router hardware. However, the effectiveness comes into question with carbon-aware routing as it heavily depends on network topology, traffic patterns, and differences in regional carbon intensity. Additionally, routing traffic through greener regions may require longer paths, potentially increasing latency and network resource consumption. 

## Connections

This papers connects well with Raha. Raha identifies network vulnerabilities under changing traffic demands and link failures. CATE's most environmentally friendly routing configuration may not be the most reliable, as can be prone to severe network degradations. As such, utilizing a combination of Raha and CATE to evaluate paths can result in greeener traffic routing, but still maintain reliability.