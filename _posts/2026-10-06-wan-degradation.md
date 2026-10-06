---
layout: post
title: "Raha: A General Tool to Analyze WAN Degradation"
date: 2026-10-05
paper_authors: "B. Arzani, S. Taheri, P. Namyar, R. Beckett, S. K. R. Kakarla, E. Jalilipour"
paper_venue: "ACM SIGCOMM 2025"
paper_url: "https://dl.acm.org/doi/epdf/10.1145/3718958.3754348"
week: 3
tags: [wan, network-degradation, failures, traffic-engineering]
---

## Key Idea

The key problem is that current WAN analysis tools only consider a small number of simulatenous failures or analyze failures and traffic changes separately, which leads to underestimating network degradation. Raha's core contribution is it is the first general tool that jointly searches across probable links failures and changing traffic demands to find scenarios that cause the greatest degradation.

## Critique

The paper convincingly demonstrates that limiting analysis to a few failures can significantly underestimate WAN degradation, in which they found scenarios with 2x greater degradation compared to existing tools. However, the limitation to this tool is that it relies on optimization and clustering so that the enormous search space is manageable, meaning the true worst-case scenario is not guaranteed. Results also depend on assumptions about failure probabilities and possible traffic demands, which may not fully reflect real life.

## Connections

This relates to previous works in the sense that G. Baltra et al's paper also suggests network failures to not be binary as current models suggest it to be. Baltra el al. show that connectivity may be partial, rather than simply up or down, while Raha shows WAN failures cannot be modeled by a small set of individual failures.

