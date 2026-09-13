---
title: "White-Light Tomography"
permalink: /projects/white-light-tomography/
project_category: tomographic-reconstructions
project_order: 2
project_image: /assets/images/projects/white-light-tomography-thumb.jpg
project_image_alt: "Reconstructed electron density and plasma velocity in a slice through a simulated coronal mass ejection."
excerpt: "Follow a solar eruption through the heliosphere in 3D. In simulation tests, SuNeRF-CME recovers CME structure from two viewpoints with a mean speed error of just 3%."
project_summary: "Follow a solar eruption through the heliosphere in 3D. In simulation tests, SuNeRF-CME recovers CME structure from two viewpoints with a mean speed error of just 3%."
---

{% include project-styles.html %}

[← Tomographic reconstructions](/projects/#tomographic-reconstructions)

**SuNeRF-CME reconstructs the changing 3D electron density of a coronal mass ejection**, turning scattered sunlight into a picture of an eruption moving through the heliosphere.

## An eruption reconstructed from two viewpoints · 2026

The method fits total and polarized white-light brightness using Thomson scattering, while physical constraints on plasma flow help resolve ambiguities between sparse views. In controlled simulation tests, two viewpoints recover CME speed with a **3.01% ± 1.94% mean error**, and propagation direction with errors of **3.39° ± 1.94° in latitude** and **1.76° ± 0.79° in longitude**. [Read the paper](https://doi.org/10.3847/1538-4357/ae6e39).

{% include project-figure.html image="/assets/images/projects/white-light-tomography-overview.jpg" alt="Two synthetic white-light viewpoints above reconstructed slices of CME electron density and plasma velocity." caption="From two synthetic camera views to a volume: reconstructed density and velocity slices show the CME 12.5 hours after launch." source_url="https://arxiv.org/html/2509.13571v2#S3.F2" source_label="Figure 2 · Jarolim et al. (2026) · CC BY 4.0" %}

The reconstruction resolves the CME's three-part structure, distorted front, and internal density variations. Additional viewpoints improve the recovered detail. **The published validation uses synthetic observations**; applying the framework to real coronagraph data is the next step toward space-weather applications.

{% include project-figure.html image="/assets/images/projects/white-light-tomography-structure.jpg" alt="Ground-truth CME density compared with reconstructions from three and two viewpoints, with corresponding error maps." caption="Slices through the simulated eruption reveal which structures survive reconstruction from only two or three viewpoints, alongside errors measured against the known density." source_url="https://arxiv.org/html/2509.13571v2#S3.F5" source_label="Figure 5 · Jarolim et al. (2026) · CC BY 4.0" %}

## Paper and code

- Jarolim, R., et al. (2026). [SuNeRF-CME: Physics-informed Neural Radiance Fields for Tomographic Reconstruction of Coronal Mass Ejections](https://doi.org/10.3847/1538-4357/ae6e39). *The Astrophysical Journal*, 1004, 168. [Open manuscript](https://arxiv.org/abs/2509.13571).
- [SuNeRF code, CME configurations, and dataset instructions](https://github.com/RobertJaro/SuNeRF#cme-tomography-white-light).
- Explore the eruption's lower-coronal setting with [EUV tomography](/projects/euv-tomography/).
