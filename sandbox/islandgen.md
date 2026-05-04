---
layout: default
title: Island Generator
permalink: /sandbox/islandgen/
---

## Demo

<div style="position:relative; padding-bottom:56%; height:0;">
  <iframe 
    src="https://cholushkin.github.io/island-generator-prototype-io"
    style="position:absolute; top:0; left:0; width:100%; height:100%; border:none; border-radius:8px;">
  </iframe>
</div>

# Island Generator

Experiment in generating islands using masks, noise, syntax-based rules, and marching cubes.

## Overview

This experiment explores procedural island generation by combining multiple techniques:

- mask-based shaping of landmass
- layered noise for terrain variation
- [syntex](https://github.com/cholushkin/SynTex) generated texture 
- marching cubes for city model

## Goals

- generate believable island silhouettes  
- maintain control over structure while allowing variation  
- experiment with combining deterministic and stochastic systems  
