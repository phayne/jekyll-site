---
layout: page
title: Diviner H-parameter
permalink: /research/datasets/diviner-h-parameter/
description: Lunar thermal inertia maps from LRO Diviner
---

<style>
.dataset-content {
  line-height: 1.7;
}
.dataset-content h2 {
  margin-top: 2rem;
  margin-bottom: 0.8rem;
  font-size: 1.2rem;
  border-bottom: 1px solid #ddd;
  padding-bottom: 0.3rem;
}
.dataset-content p {
  margin-bottom: 1rem;
}
.dataset-meta {
  background: #f5f5f5;
  padding: 1rem;
  border-radius: 6px;
  margin-bottom: 1.5rem;
  font-size: 0.9rem;
}
.dataset-meta dt {
  font-weight: 600;
  display: inline;
}
.dataset-meta dd {
  display: inline;
  margin-left: 0;
  margin-right: 1.5rem;
}
.download-button {
  display: inline-block;
  background: #0066cc;
  color: white;
  padding: 0.6rem 1.2rem;
  border-radius: 4px;
  text-decoration: none;
  font-size: 0.95rem;
  margin-top: 0.5rem;
}
.download-button:hover {
  background: #0055aa;
  color: white;
}
.back-link {
  margin-top: 2rem;
  font-size: 0.9rem;
}
.back-link a {
  color: #0066cc;
  text-decoration: none;
}
.back-link a:hover {
  text-decoration: underline;
}
</style>

<div class="dataset-content">

<div class="dataset-meta">
  <dl>
    <dt>Source:</dt> <dd>LRO Diviner Lunar Radiometer</dd>
    <dt>Coverage:</dt> <dd>±70° latitude</dd>
    <dt>Resolution:</dt> <dd>128 pixels per degree</dd>
    <dt>Format:</dt> <dd>32-bit floating point</dd>
  </dl>
</div>

The H-parameter is a measure of thermal inertia derived from Diviner Lunar Radiometer observations aboard the Lunar Reconnaissance Orbiter. These maps characterize the thermophysical properties of the upper few centimeters of the lunar regolith.

## Dataset Contents

The data directory contains:

- **H-parameter maps** — Values in meters, representing the characteristic depth scale of diurnal temperature variations
- **Latitude and longitude grids** — Corresponding coordinate arrays for georeferencing
- **Thermal inertia maps** — Derived thermal inertia referenced to 273 K, at 10 pixels per degree resolution

## Scientific Background

The H-parameter describes how temperature waves propagate into the lunar subsurface during the day-night cycle. It is related to thermal inertia (Γ) by:

H = Γ / (ρc)

where ρ is density and c is specific heat capacity. Higher H values indicate coarser or more consolidated surface materials, while lower values suggest fine-grained regolith.

## Usage Notes

Data files are provided in binary floating-point format. The maps span -70° to +70° latitude at 128 pixels per degree resolution. Polar regions (|latitude| > 70°) require different analysis approaches due to the extreme thermal environment.

## Citation

If you use these data in your research, please cite:

> Hayne, P.O., et al. (2017). Global regolith thermophysical properties of the Moon from the Diviner Lunar Radiometer Experiment. *Journal of Geophysical Research: Planets*, 122, 2371–2400. [doi:10.1002/2017JE005387](https://doi.org/10.1002/2017JE005387)

<a href="https://goo.gl/JhMGs5" target="_blank" class="download-button">Download Dataset</a>

</div>

<div class="back-link">
  ← <a href="/research/">Back to Research</a>
</div>
