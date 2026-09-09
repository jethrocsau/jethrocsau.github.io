---
title: "Inspect-REPA: When, Where, and How Long Should Diffusion Models Align Representations?"
summary: Study on scheduling representation-alignment loss in diffusion transformers, across baseline, early-stop, and cosine-annealed schedules on ImageNet-100.
date: "2026-09-09"
authors:
  - admin
tags:
  - Diffusion Models
  - Representation Alignment
  - Generative AI
image:
  caption: 'Inspect-REPA cover'
# Display this page in the Featured widget?
featured: true
---

Representation alignment is usually trained as a static, always-on auxiliary loss for diffusion transformers. This project (with Tianyu Zhao) asks whether that assumption is necessary — studying the question in three stages on a SiT-B/2 backbone trained on ImageNet-100 at 256px latent diffusion: validating the baseline ordering and layer placement, testing hard early-stop schedules for the projection term, and evaluating long-horizon cosine annealing over 250k steps.

**[Read the full write-up →](/auto-repa-blog/)**

[Source Code](https://github.com/zhaotianyu0702/Auto-REPA)
