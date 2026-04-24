---
layout: post
title:  Artemis II Astronaut Photographs — Validation of 3D Moon Simulations
date:   2026-04-23 00:00:00
description: Comparing our 3D ray-traced lunar illumination model to photographs taken by the Artemis II crew during their lunar flyby.
---

During the <a href="https://www.nasa.gov/mission/artemis-ii/" target="_blank">Artemis II</a> lunar flyby, the crew photographed the Moon with high‑resolution handheld cameras from a trajectory available in standard ephemeris format through <a href="https://ssd.jpl.nasa.gov/" target="_blank">JPL's Horizons system</a>. NASA has released a trove of <a href="https://www.nasa.gov/artemis-ii-multimedia/" target="_blank">Artemis II imagery and video</a> from the flyby. These photographs are a useful validation dataset for physics‑based models of lunar illumination — models that compute how sunlight scatters from the cratered surface, where shadows fall, and how the terminator expresses the local topography. These studies are motivated by planning for the Artemis crewed surface missions, which will explore and conduct science in the Moon's south polar region, where shadows are stark and temperatures are extreme. This post compares Artemis II imagery with synthetic imagery from our group's 3D ray‑traced lunar illumination and thermophysical model, <b>PTM3D</b>.

<img style="display: block; width: 100%; height: auto; margin: 20px 0;"
     src="{{ site.baseurl }}/assets/img/artemis-ii-flyby-ptm3d-compare.png"
     alt="Artemis II photograph of the Moon compared with a PTM3D synthetic image for the same viewing geometry"
     title="PTM3D vs. Artemis II"/>
<div class="col three caption">
    (Left) <a href="https://www.nasa.gov/image-detail/amf-art002e009287/" target="_blank">Nikon D5 photograph</a> from the Artemis II spacecraft during the lunar flyby, showing the sunlit crescent of the Moon with a crescent Earth beyond the lunar limb (photo credit: NASA).
    (Right) PTM3D synthetic image for the same camera viewpoint, solar illumination, and Earth–Moon geometry; simulation time 2026‑04‑06 21:01 UTC.
</div>

<h4>What is PTM3D?</h4>

PTM3D is a planetary thermophysical model that pairs full 3D ray‑tracing of solar and thermal illumination with a subsurface heat‑conduction solver, building on the first such 3D thermal model for planetary science, introduced for the lunar south polar cold traps by Paige et al. (2010)<sup><a href="#ref-paige2010">[1]</a></sup>. Rather than approximating the surface as a flat facet or a smooth sphere, PTM3D works directly on high‑resolution digital terrain models of the Moon (from <a href="https://pds-geosciences.wustl.edu/missions/lro/lola.htm" target="_blank">LRO/LOLA</a>), accounting for local slopes, scattering from nearby terrain, self‑shadowing inside craters, and reflected and re‑emitted radiation from surrounding surfaces. We developed it to simulate thermal environments inside permanently shadowed regions (PSRs) near the lunar poles, where reflected sunlight and infrared emission from nearby illuminated terrain are often the <i>dominant</i> energy source. The same model can produce synthetic imagery for any camera viewpoint, at any wavelength, for any solar geometry, which makes it a useful tool to compare against the Artemis II photographs.

<h4>The validation setup</h4>

The Artemis II crew carried a suite of Nikon D5 bodies with lenses ranging from wide‑angle to long telephoto; the photograph shown above was taken with a zoom lens somewhere in the 80–200&nbsp;mm range<sup><a href="#ref-space-gear">[2]</a></sup>. The PTM3D simulation was generated at a 50&nbsp;mm equivalent focal length, so differences in magnification and framing between the two images reflect the optical mismatch rather than a disagreement in the underlying physics. We modeled the Artemis II trajectory with a synthetic pinhole camera pointed at the sub‑spacecraft point, and set the solar vector and Earth–Moon–Sun geometry from JPL Horizons ephemerides for the moment of exposure. The simulation uses a Lommel‑Seeliger photometric function for the regolith; no photometric tuning was applied between the two images.

We also have independent radiometric and temperature data from the <b><a href="https://www.diviner.ucla.edu/" target="_blank">Diviner Lunar Radiometer Experiment</a></b><sup><a href="#ref-diviner">[3]</a></sup> covering the same terrain captured by the Artemis II Nikon frames. That provides an absolute‑calibrated second channel for cross‑checking PTM3D alongside the visible astronaut photographs. In parallel, we compare PTM3D against high‑resolution images from the <a href="https://lroc.im-ldi.com/" target="_blank">Lunar Reconnaissance Orbiter Camera (LROC)</a>, which are useful for local models where high‑resolution DTMs are available; the Artemis II flyby images are complementary in that they provide a unique opportunity to test the global‑scale lunar model together with the solar and Earth geometry.

<h4>Flyby animation</h4>

Stepping the synthetic camera along the Artemis II<sup><a href="#ref-artemis2">[4]</a></sup> trajectory turns the static comparison into a sequence. The animation below spans 180 frames at 2‑minute cadence, from 2026‑04‑06 21:01 UTC to 2026‑04‑07 02:59 UTC, with the Nikon D5 + 50&nbsp;mm optics fixed and only the spacecraft viewpoint varying with time.

<video controls autoplay loop muted playsinline preload="metadata"
       style="display: block; width: 100%; max-width: 900px; height: auto; margin: 20px auto;">
    <source src="{{ site.baseurl }}/assets/img/artemis2-ptm3d-flyby.mp4" type="video/mp4"/>
    Your browser does not support embedded video.
</video>
<div class="col three caption">
    PTM3D synthetic imagery across the Artemis II flyby at Nikon D5 + 50&nbsp;mm. The lunar crescent widens and the terminator rotates across the nearside–farside boundary as the spacecraft arcs around the Moon.
</div>

The animation confirms that the same illumination physics used for polar thermal modeling reproduces the viewing geometry and terminator motion observed from Artemis II across the full flyby.

<h4>Earthshine</h4>

PTM3D includes earthshine — sunlight reflected off the Earth onto the lunar nightside — as a secondary illumination source. It isn't apparent in the standard visible image because the directly sunlit crescent is orders of magnitude brighter than the earth‑lit nightside. Isolating the earthshine channel reveals the component on its own:

<img style="display: block; width: 100%; max-width: 800px; height: auto; margin: 20px auto;"
     src="{{ site.baseurl }}/assets/img/artemis-ii-flyby-ptm3d-earthshine.png"
     alt="PTM3D synthetic image showing earthshine-only illumination of the lunar nightside"
     title="PTM3D earthshine channel"/>
<div class="col three caption">
    PTM3D simulation of the earthshine component only, for the same Artemis II viewing geometry. The Moon's nightside is indirectly illuminated by sunlight reflected from Earth; the bright disk at left is the Sun, and the directly sunlit crescent appears along the left limb.
</div>

<h4>What the comparison validates</h4>

What this first pass validates:
<ul>
<li>The camera viewpoint and timing — ephemerides, spacecraft attitude, and the transformation into the PTM3D reference frame — are consistent enough to place lunar features in the correct part of the image.</li>
<li>First‑order illumination geometry: terminator position, crescent width, and the direction of shadows on large craters.</li>
<li>Large‑scale topographic self‑shadowing at grazing solar angles; the ragged terminator is a direct expression of the DTM.</li>
<li>The presence and qualitative distribution of earthshine on the nightside, visible in the dedicated earthshine image above.</li>
</ul>

Caveats:
<ul>
<li>The Nikon D5 photograph was taken at an 80–200&nbsp;mm equivalent focal length, while the PTM3D simulation used 50&nbsp;mm. Differences in apparent size and framing between the two crescents are driven by that magnification mismatch, not by the model.</li>
<li>The Nikon D5 is a visible‑band sensor, so only reflected light is being compared in these frames. PTM3D's thermal emission is cross‑checked instead against Diviner Lunar Radiometer data for the same terrain, drawing on the global regolith thermophysical properties characterized by Hayne et al. (2017)<sup><a href="#ref-hayne2017">[5]</a></sup>.</li>
</ul>

<h4>Why this matters for the first Artemis crewed surface mission</h4>

The first Artemis crewed surface mission will put astronauts on the lunar surface near the south pole, in terrain where illumination changes substantially over short distances and short times. Planners need to know, at meter‑scale resolution, when a given boulder will cast a shadow long enough to threaten a traverse, when a communications asset will drop into darkness, and when a hazard camera will be pointed at a low‑elevation Sun. A model that has been cross‑checked against Artemis II astronaut photography — where ground truth and spacecraft geometry are both well documented — is more trustworthy for those higher‑stakes operational questions. The same simulations also support training activities and mission rehearsals.

As an example, the animation below shows PTM3D‑simulated overhead surface temperatures near Haworth crater at the lunar south pole — an illustrative site, not one of the candidate Artemis landing sites — over a full lunar day. The region shown spans roughly 15&nbsp;km across, with a mesh resolution of 5&nbsp;m at the center. Permanently shadowed regions remain at cryogenic temperatures throughout, while sunlit highlands swing by hundreds of kelvin across day/night cycles.

<video controls autoplay loop muted playsinline preload="metadata"
       style="display: block; width: 100%; max-width: 900px; height: auto; margin: 20px auto;">
    <source src="{{ site.baseurl }}/assets/img/haworth-ptm3d-surface-temperature.mp4" type="video/mp4"/>
    Your browser does not support embedded video.
</video>
<div class="col three caption">
    PTM3D overhead view of simulated surface temperatures near Haworth crater (lunar south pole) across a lunar day. The region spans roughly 15&nbsp;km across, with a mesh resolution of 5&nbsp;m at the center. This site is shown as an illustrative example and is not one of the Artemis candidate landing sites.
</div>

<h4>What's next</h4>

With PTM3D's illumination and thermal physics grounded by the Artemis II comparison, the next step is to apply the model to the Artemis surface mission candidate landing sites near the lunar south pole. That means:
<ol>
<li>Running PTM3D at high spatial resolution over each candidate landing region to simulate surface and subsurface temperatures through a full lunar day, including the prolonged shadowing that dominates the polar thermal environment.</li>
<li>Using those temperature histories to predict water ice stability — where ice can persist on or just beneath the surface, and over what timescales — including the small‑scale cold traps identified by Hayne et al. (2021)<sup><a href="#ref-hayne2021">[6]</a></sup>.</li>
<li>Delivering illumination and thermal products that feed into traverse planning, instrument placement, and resource‑utilization decisions for crewed and robotic surface operations.</li>
<li>Simulating landing sites for NASA's <a href="https://www.nasa.gov/commercial-lunar-payload-services/" target="_blank">Commercial Lunar Payload Services</a> (CLPS) program, including the upcoming CP-22 mission carrying <a href="https://lasp.colorado.edu/instruments/l-ciris/" target="_blank">L-CIRiS</a>, a lunar thermal infrared imager led by LASP and built at BAE Systems in Boulder, Colorado.</li>
</ol>

Because the Artemis II comparison gives us confidence that PTM3D reproduces real lunar illumination and its coupling to the thermophysical state of the surface, the landing‑site predictions carry a direct observational constraint rather than resting on first‑principles extrapolation alone.

<h4><a id="references">References</a></h4>
<ol>
  <li><a id="ref-paige2010">Paige, D. A., Siegler, M. A., Zhang, J. A., <u>Hayne, P. O.</u>, et al. (2010). Diviner Lunar Radiometer observations of cold traps in the Moon's south polar region. <i>Science, 330</i>, 479–482. <a href="https://doi.org/10.1126/science.1187726" target="_blank">doi:10.1126/science.1187726</a>.</a></li>
  <li><a id="ref-space-gear">Artemis II camera gear (Nikon D5 bodies with 50&nbsp;mm and 80–200&nbsp;mm zoom lenses). <a href="https://www.space.com/stargazing/skywatching-kit/nasa-took-this-camera-gear-to-space-aboard-artemis-2-and-you-can-own-it-too" target="_blank">space.com feature</a>.</a></li>
  <li><a id="ref-diviner">Diviner Lunar Radiometer Experiment (UCLA / LRO). <a href="https://www.diviner.ucla.edu/" target="_blank">diviner.ucla.edu</a>.</a></li>
  <li><a id="ref-artemis2">Artemis II mission overview — <a href="https://www.nasa.gov/mission/artemis-ii/" target="_blank">nasa.gov/mission/artemis-ii</a>.</a></li>
  <li><a id="ref-hayne2017"><u>Hayne, P. O.</u>, Bandfield, J. L., Siegler, M. A., Vasavada, A. R., Ghent, R. R., Williams, J.-P., <i>et al.</i> (2017). Global regolith thermophysical properties of the Moon from the Diviner Lunar Radiometer Experiment. <i>Journal of Geophysical Research: Planets, 122</i>, 2371–2400. <a href="https://doi.org/10.1002/2017JE005387" target="_blank">doi:10.1002/2017JE005387</a>.</a></li>
  <li><a id="ref-hayne2021"><u>Hayne, P. O.</u>, Aharonson, O., &amp; Schörghofer, N. (2021). Micro cold traps on the Moon. <i>Nature Astronomy, 5</i>, 169–175. <a href="https://doi.org/10.1038/s41550-020-1198-9" target="_blank">doi:10.1038/s41550-020-1198-9</a>.</a></li>
</ol>

<hr style="margin-top: 40px; margin-bottom: 20px;">
<div style="display: flex; align-items: flex-start; gap: 20px; margin: 20px 0; font-size: 0.85em; line-height: 1.5;">
    <img src="{{ site.baseurl }}/assets/img/prof_pic.jpg"
         alt="Paul Hayne"
         style="width: 90px; height: auto; border-radius: 4px; flex-shrink: 0;"/>
    <div>
        <b>About the author.</b> Paul Hayne is an associate professor in the <a href="https://www.colorado.edu/aps" target="_blank">Astrophysical &amp; Planetary Sciences Department</a> and the <a href="https://lasp.colorado.edu" target="_blank">Laboratory for Atmospheric &amp; Space Physics</a> at the University of Colorado Boulder. His research focuses on the thermal behavior of terrestrial planets and moons, especially icy worlds, using data from spacecraft and Earth‑based observatories to investigate planetary atmospheres and surfaces.
    </div>
</div>
