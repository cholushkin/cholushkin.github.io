---
layout: default
title: Island Generator
permalink: /sandbox/islandgen/
---

# Procedural Island Generator

Interactive browser-based procedural island generator exploring a modular terrain-generation pipeline.

## Demo

<div style="position:relative; padding-bottom:56%; height:0;">
  <iframe
    src="https://cholushkin.github.io/island-generator-prototype-io"
    style="position:absolute; top:0; left:0; width:100%; height:100%; border:none; border-radius:8px;">
  </iframe>
</div>

<p style="margin-top:12px;">
  <a href="https://cholushkin.github.io/island-generator-prototype-io" target="_blank" rel="noopener">
    ▶ Run Fullscreen ↗
  </a>
</p>

👉 [Demo repo ↗](https://github.com/cholushkin/island-generator-prototype-io)  
👉 [Readme ↗](https://github.com/cholushkin/island-generator-prototype-io/blob/master/README.md)  
👉 [Ideas ↗](https://github.com/cholushkin/island-generator-prototype-io/blob/master/ideas.md)  
👉 [Syntex ↗](https://github.com/cholushkin/SynTex)

## Project Showcase

A procedural terrain-generation prototype built around a modular data pipeline. Each stage transforms field data, making it possible to experiment with terrain generation, masking, city placement, and geometry generation independently.

**Pipeline:** Noise → Mask → Syntex → Marching Cubes

**Focus:**
- Layered noise terrain generation
- Terrain-aware city placement
- Syntex-based procedural cities
- Modular node-based processing
- Marching Cubes terrain generation

Prototype for future Unity integration.