---
layout: post
title: "Understanding Partial Reachability in the Internet Core"
date: 2026-09-30
paper_authors: "G. Baltra, T. Saluja, Y. Pradkin, J. Heidemann"
paper_venue: "NINeS 2026"
paper_url: "https://2026.nines-conference.org/papers/p004-Baltra.pdf"
week: 2
tags: [reachability, routing, outages, internet-core]
---

## Key Idea

The key problem is that the problem of the Internet today isn't that is it reachable or unreachable, but rather that networks can be partially reachable. It's core contribution is defining islands (computers partitioned from the Internet core) and peninsulas (partial connectivity), and introducing algorithms Taitao and Chiloe to detect partial reachability events and demonstrate partial reachability as a fundamental part of the Internet.

## Critique

The paper convincingly demonstrates partial reachability as a real and significant problem of the Internet, using independent measurement systems such as CAIDA Ark and applies them to large datasets from Trinocular and RIPE Atlas. The limitation, however, to the approach taken in the paper is that it heavily depends on the placements of the vantage points. For example, for the Taitao algorithm if the vantage points are put on similar routing paths, thus on the same side of a connectivity failure, peninsulas can go undetected.

## Connections

This relates to the previous (and first) reading as both the readings challenges assumptions of the how the Internet behaves. Misa et al. Both readings utilizes empirical measurements to demonstrate underlying Internet behaviors that have been underobserved.

