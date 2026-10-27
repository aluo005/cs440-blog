---
layout: post
title: "Simulate Before Sending: Rethinking Transport in Datacenter Networks"
date: 2026-10-21
paper_authors: "D. Straussman, I. Keslassy, A. Shpiner, L. Liss"
paper_venue: "NINeS 2026"
paper_url: "https://2026.nines-conference.org/papers/p019-Straussman.pdf"
week: 5
tags: [datacenter-networks, transport-protocols, congestion-control, packet-loss, ai-training]
---

## Key Idea

The key problem is that existing datacenter transport protocols suffer from packet losses and retransmissions, which significantly increase the collect completion times for AI training workloads. This paper's core contribution is dcSim, a transport mechanism that can send small simulation packets to probe network congestion, and then transmitting the actual data packets along successful paths, achieving practically lossless communication and faster completion times using commodity switches.

## Critique

The paper convincingly demonstrates that dcSim can reduce packet losses and improve collective completion times, even under challenging network conditions such as oversubscribed links. However, its approach introduces additional overhead from simulation packets and acknowledgements, as as delays before actual data transmission. Furthermore, successful simulation packets to not guarantee that subsequent data packets will avoid congestion, particularly in complex multi-stage networks. 

## Connections

This paper connects to P-ECMP becuase they both explore alternative approahces to managing network congestion and improving performance. P-ECMP enables precise traffic rerouting using existing hardware, while dcSim proactively probes network paths before transmitting data, demonstrating another approach in using network congestion information to improve performance without requiring specialized switches.