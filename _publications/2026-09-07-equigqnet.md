---
title: "EquiGQNet: Fast Grasp Quality Evaluation via Shared Equivariant Point Cloud Encoding"
collection: publications
category: preprints
permalink: /publication/2026-09-07-equigqnet
excerpt: 'EquiGQNet evaluates 6-DoF grasp candidates for unseen objects in cluttered scenes from a single depth image. An SO(3)-equivariant encoder processes the scene once and rotates the features per grasp, while grasp positions are injected into intermediate layers to keep local geometry tied to each candidate, giving a 6.9x faster CEM planning loop.'
date: 2026-09-07
authors: 'Sungwon Seo, Jaeseog Won, Jiyou Shin, Youngjin Seo, <b>Hyunjun Kim</b>, Seokmin Yoon, Tuan Luong, Hyungpil Moon'
venue: 'arXiv preprint arXiv:2609.07145'
header:
  teaser: publications/equigqnet.png
paperurl: 'https://arxiv.org/abs/2609.07145'
projecturl: 'https://equigqnet.github.io/'
citation: 'Sungwon Seo, Jaeseog Won, Jiyou Shin, Youngjin Seo, <b>Hyunjun Kim</b>, Seokmin Yoon, Tuan Luong, and Hyungpil Moon. (2026). &quot;EquiGQNet: Fast Grasp Quality Evaluation via Shared Equivariant Point Cloud Encoding.&quot; <i>arXiv preprint</i> arXiv:2609.07145.'
---

EquiGQNet is a grasp quality network for evaluating 6-DoF grasp candidates on unseen objects in cluttered tabletop scenes from a single depth image. It combines the strengths of early and late fusion: the scene is encoded once with an SO(3)-equivariant encoder and the shared features are rotated for each grasp, while grasp positions are injected into intermediate layers so that local geometry stays tied to each candidate.

In simulation, it achieves grasp performance close to an early-fusion baseline, clearly outperforms late fusion on hard geometries, and cuts CEM planning time by 6.9x (3.31s to 0.48s). In real-world decluttering experiments, it reaches a 95.2% grasp success rate at 230 picks per hour.
