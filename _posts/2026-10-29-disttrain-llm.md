---
layout: post
title: "DistTrain: Addressing Model and Data Heterogeneity with Disaggregated Training for Multimodal Large Language Models"
date: 2026-10-28
paper_authors: "Z. Zhang, Y. Zhong, Y. Jiang, H. Hu, J. Sun, Z. Ge, Y. Zhu, D. Jiang, X. Jin"
paper_venue: "ACM SIGCOMM 2025"
paper_url: "https://dl.acm.org/doi/10.1145/3718958.3750472"
week: 6
tags: [distributed-training, multimodal-llms, gpu-utilization, disaggregation, scheduling]
---

## Key Idea

The key problem is training multimodel LLMs suffers from low GPU utilization due to model and data heterogeneity, where different model components and data modalities require different amounts of computation. The paper's core contribution is DistTrain, a disaggregated training framework that independenly manages resources for different model components and separates data preprocessing from training, thus reduces bottlenecks and achieving up to 2.2x higher training throughput compared to Megatron-LM.

## Critique

The paper convincingly demonstrates that disaggregating model components and data preprocessing can significantly improve training efficiency, achieving 54.7% GPU Model FLOPs utilization when training 72B-parameter model across 1172 GPUs. However, the tradeoff of this is the increased overhead due to more communication, limiting performance when bandwidth is constrained. Additionally, evaluation focuses on large-scale production GPU cluster, so benefits may not generalize to smaller clusters with fewer available resources.

## Connections

This paper connects to dcSim and P-ECMP in the sense those can be integrated to improve efficiency of distributed multimodel LLM training. Since DistTrain separates model components across different GPUs, efficient communication is extremely important. By using dcSim for packet loss reduction, and P-ECMP for better network pathing, it can potentially push GPU utilization even further by reducing network bottlnecks introduced by disaggregated training.