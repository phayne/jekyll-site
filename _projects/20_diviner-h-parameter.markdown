---
layout: page
title: Diviner H-parameter
description: lunar thermal inertia maps
img: /assets/img/research/diviner-h.jpg
---

The H-parameter is a measure of subsurface structure derived from Diviner Lunar Radiometer observations aboard the Lunar Reconnaissance Orbiter. These maps characterize the thermophysical properties of the upper few centimeters of the lunar regolith.

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

- **H-parameter maps** — Values in meters, representing the e-folding depth scale of the regolith density and conductivity profiles
- **Latitude and longitude grids** — Corresponding coordinate arrays for georeferencing
- **Thermal inertia maps** — Derived thermal inertia referenced to 273 K, at 10 pixels per degree resolution

#### Scientific Background

The H-parameter describes the characteristic length scale over which regolith density and thermal conductivity increase with depth due to compaction. It is the e-folding depth of the exponential density and conductivity profiles in the upper regolith.

Lower H values indicate more rapid densification with depth, corresponding to higher thermal inertia materials such as rocks or consolidated regolith. Higher H values indicate a more gradual density profile, characteristic of fine-grained, porous regolith with lower thermal inertia.

#### Download

<a href="https://o365coloradoedu-my.sharepoint.com/:f:/g/personal/paha3326_colorado_edu/Ek_HjDuQUIVPnvCyh2gpWWIBFtlDaEM3ESSqr9URoh6u5Q" target="_blank" class="btn btn-primary">Download Dataset</a>

#### Related Publications

<div class="publications">
<ul>
<li><u>Hayne, P. O.</u>, Bandfield, J. L., Siegler, M. A., Vasavada, A. R., Ghent, R. R., Williams, J.-P., Greenhagen, B. T., Aharonson, O., Elder, C. M., Lucey, P. G., &amp; Paige, D. A. (2017). Global regolith thermophysical properties of the Moon from the Diviner Lunar Radiometer Experiment. <i>Journal of Geophysical Research: Planets, 122</i>, 2371–2400.
<a href="https://doi.org/10.1002/2017JE005387" target="_blank">Link</a></li>
<li>Vasavada, A. R., Bandfield, J. L., Greenhagen, B. T., <u>Hayne, P. O.</u>, Siegler, M. A., Williams, J.-P., &amp; Paige, D. A. (2012). Lunar equatorial surface temperatures and regolith properties from the Diviner Lunar Radiometer Experiment. <i>Journal of Geophysical Research: Planets, 117</i>, E00H18.
<a href="https://doi.org/10.1029/2011JE003987" target="_blank">Link</a></li>
</ul>
</div>
