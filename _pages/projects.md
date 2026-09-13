---
permalink: /projects/
title: "Projects"
excerpt: "Reconstructing the Sun in 3D, revealing the magnetic fields behind eruptions, and turning solar observations into new scientific discoveries with AI."
---

{% include project-styles.html %}

<p class="research-intro">What powers a solar eruption? What does the far side of the Sun look like? My research combines solar physics and AI to recover the hidden structure of the solar atmosphere and extract more science from every observation.</p>

Explore the results below, with figures from the papers, links to the research, and open-source tools.

<nav class="research-nav" aria-label="Research areas">
  <a href="#magnetic-field-simulations">Magnetic fields</a>
  <a href="#tomographic-reconstructions">3D tomography</a>
  <a href="#image-enhancement">Image enhancement</a>
  <a href="#solar-feature-detection">Solar features</a>
  <a href="#spectropolarimetric-inversions">Spectropolarimetry</a>
</nav>

## Magnetic Field Simulations
{: .research-section }

Reveal the magnetic architecture that powers solar activity. Physics-informed neural networks connect surface measurements to three-dimensional coronal fields, trace the energy released by flares, and incorporate chromospheric observations to resolve hidden flux ropes.

{% include project-cards.html category="magnetic-field-simulations" %}

## Tomographic Reconstructions
{: .research-section }

Turn flat images into evolving, three-dimensional views of the Sun. SuNeRF reconstructs the EUV corona from multiple spacecraft; SuNeRF-CME extends the approach to the density and motion of erupting plasma in white light.

{% include project-cards.html category="tomographic-reconstructions" %}

## Image Enhancement
{: .research-section }

Connect decades of observations and recover fine solar structure. These methods harmonize instruments, identify degraded images, and reconstruct ground-based observations affected by Earth's atmosphere.

{% include project-cards.html category="image-enhancement" %}

## Solar Feature Detection
{: .research-section }

Follow the structures that shape space weather: coronal holes that feed the solar wind and filaments that can erupt. Automated detection turns large solar archives into consistent maps of activity.

{% include project-cards.html category="solar-feature-detection" %}

## Spectropolarimetric Inversions
{: .research-section }

Read the Sun's magnetic fingerprints in polarized light. A continuous neural representation couples neighboring measurements in space and time, helping recover coherent magnetic structure from noisy spectra.

{% include project-cards.html category="spectropolarimetric-inversions" %}

For complete author lists and publication details, see [Publications]({{ '/publications/' | relative_url }}). Figure captions link to their original sources; click a figure on a project page to open the full image.
