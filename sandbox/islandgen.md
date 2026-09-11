---
layout: default
title: Island Generator
permalink: /sandbox/islandgen/
---

# Procedural Island Generator

Interactive browser-based procedural island generator exploring a modular terrain-generation pipeline.

## Demo

<div style="margin-bottom:12px;">
  <button
    type="button"
    onclick="document.getElementById('island-generator-frame').requestFullscreen()">
    ⛶ Fullscreen
  </button>
</div>

<div style="
  width:100vw;
  margin-left:calc(50% - 50vw);
  height:calc(100vh - 120px);
  min-height:700px;
">
  <iframe
    id="island-generator-frame"
    src="https://cholushkin.github.io/island-generator-prototype-io"
    allow="fullscreen"
    style="
      width:100%;
      height:100%;
      border:none;
    ">
  </iframe>
</div>

👉 [Full demo ↗](https://cholushkin.github.io/island-generator-prototype-io)  
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