---
title: "Image Quality Assessment"
permalink: /projects/image-quality-assessment/
project_category: image-enhancement
project_order: 2
project_image: /assets/images/projects/image-quality-assessment-figure4.webp
project_image_alt: "Solar H-alpha observations with maps identifying clouds and other image degradation."
excerpt: "Find the clear views in a flood of solar images. A neural quality metric separates clear and degraded observations with 98.5% accuracy and pinpoints affected regions."
project_summary: "Find the clear views in a flood of solar images. A neural quality metric separates clear and degraded observations with 98.5% accuracy and pinpoints affected regions."
---

{% include project-styles.html %}

[Projects](/projects/) / [Image enhancement](/projects/#image-enhancement)

Clouds, contrails, and instrumental faults can masquerade as changes on the Sun. Automated image-quality assessment identifies these problems quickly, helping observatories select observations that scientists and detection algorithms can trust.

## Finding degradation without a reference image

**Jarolim et al. (2020), Astronomy & Astrophysics.** A generative neural network learns the appearance of high-quality Hα observations. When it reconstructs an unfamiliar cloud or instrumental artifact poorly, the difference reveals both the severity and location of the degradation.

Tested on Kanzelhöhe observations spanning **2012–2019**, the best model distinguished clear and degraded images with **98.5% accuracy** and a true skill statistic of **0.97**. Its continuous score follows human judgments, while inference took about **17 milliseconds** in the reported implementation. Once trained, it needs no simultaneous high-quality reference.

{% include project-figure.html image="/assets/images/projects/image-quality-assessment-figure4.webp" alt="Three rows of H-alpha images, reconstruction differences, and red masks showing regions affected by atmospheric degradation." caption="The quality metric locates the problem: original images at left, reconstruction differences in the middle, and affected regions highlighted at right." source_url="https://arxiv.org/abs/2008.12030" source_label="Figure 4 · Jarolim et al. (2020), author manuscript" %}

[Read the paper](https://doi.org/10.1051/0004-6361/202038691) · [Open manuscript](https://arxiv.org/abs/2008.12030) · [Code](https://github.com/RobertJaro/SolarImageQualityAssessment)

The [Kanzelhöhe data-products study](https://doi.org/10.1007/s11207-021-01903-4) places this quality metric in the wider observatory workflow and compares it with image sharpness. Related [Instrument-to-Instrument Translation](/projects/instrument-to-instrument-translation/) uses quality assessment to help select solar images for enhancement.
