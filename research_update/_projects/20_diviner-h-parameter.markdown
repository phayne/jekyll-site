---
layout: page
title: Diviner H-parameter
description: lunar thermal inertia maps
img: /assets/img/research/diviner-h.jpg
---

The H-parameter is a measure of thermal inertia derived from Diviner Lunar Radiometer observations aboard the Lunar Reconnaissance Orbiter. These maps characterize the thermophysical properties of the upper few centimeters of the lunar regolith.

<div class="img_row">
    <img class="col three" src="{{ site.baseurl }}/assets/img/h-parameter-map.jpg" alt="H-parameter map" title="Global H-parameter map"/>
</div>
<div class="col three caption">
    Global map of the H-parameter derived from Diviner observations, revealing variations in regolith structure across the lunar surface.
</div>

#### Dataset Information

| Property | Value |
|----------|-------|
| **Source** | LRO Diviner Lunar Radiometer |
| **Coverage** | ±70° latitude |
| **Resolution** | 128 pixels per degree |
| **Format** | 32-bit floating point |

#### Dataset Contents

The data directory contains:

- **H-parameter maps** — Values in meters, representing the characteristic depth scale of diurnal temperature variations
- **Latitude and longitude grids** — Corresponding coordinate arrays for georeferencing
- **Thermal inertia maps** — Derived thermal inertia referenced to 273 K, at 10 pixels per degree resolution

#### Scientific Background

The H-parameter describes how temperature waves propagate into the lunar subsurface during the day-night cycle. It is related to thermal inertia (Γ) by:

H = Γ / (ρc)

where ρ is density and c is specific heat capacity. Higher H values indicate coarser or more consolidated surface materials, while lower values suggest fine-grained regolith.

#### Usage Notes

Data files are provided in binary floating-point format. The maps span -70° to +70° latitude at 128 pixels per degree resolution. Polar regions (|latitude| > 70°) require different analysis approaches due to the extreme thermal environment.

#### Download

<a href="https://goo.gl/JhMGs5" target="_blank" class="btn btn-primary">Download Dataset</a>

<div class="publications">
<h4>Citation</h4>
<p>If you use these data in your research, please cite:</p>
<ul>
<li><u>Hayne, P. O.</u>, Bandfield, J. L., Siegler, M. A., Vasavada, A. R., Ghent, R. R., Williams, J.-P., ... & Paige, D. A. (2017). Global regolith thermophysical properties of the Moon from the Diviner Lunar Radiometer Experiment. <i>Journal of Geophysical Research: Planets, 122</i>, 2371–2400.
<a href="https://doi.org/10.1002/2017JE005387" target="_blank">Link</a></li>
</ul>
</div>
