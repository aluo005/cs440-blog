---
layout: post
title: "OpenFLAME: A Federated Spatial Naming Infrastructure"
date: 2026-11-04
paper_authors: "S. Bharadwaj, Z. Ma, I. Liang, M. Farb, A. Rowe, S. Seshan"
paper_venue: "NINeS 2026"
paper_url: "https://2026.nines-conference.org/papers/p020-Bharadwaj.pdf"
week: 7
tags: [spatial-naming, federated-systems, network-infrastructure, location-based-services]
---

## Key Idea

The key problem is that existing mapping systems, such as Google Maps and Apple Maps, are centralized and primarily cover outdoor spaces, making it difficult to integrate private indoor maps for applications such as augmented reality and robotics. The paper's core contribution is OpenFLAME, a federated spatial naming infrastructure that uses DNS-based discovery that allows independent organizations to manage their own maps while also enabling applications to discover/combine mapping services across different regions.

## Critique

The paper convincingly demonstrates that existing DNS infrastructure can support a scalable federated mapping system while preserving independent ownership and access control of spatial data. However, distributing the maps across different serves can also introduce additional discovery and routing overhead. For example, federated routing takes around twice as long as centralized routing at the median and produces path 12% longer on average on median. Also, overlapping maps from independent provides can create some conflicts thus complicating service discovery.

## Connections

This paper connects to both P-ECMP and QUIC deployment. OpenFLAME leverages DNS to discover independently managed map servers, which can connect with P-ECMP in which provides more precise traffic control. P-ECMP can improve path selection for communication between OpenFLAME clients and distributed map servers. Additionally, QUIC load-balancing measurements can help inform OpenFLAME on how it can distribute requests acorss geographically dispersed mapping services.