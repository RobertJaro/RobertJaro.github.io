---
title: "Coronal Holes"
permalink: /projects/coronal-holes/
project_category: solar-feature-detection
project_order: 1
project_image: /assets/images/projects/coronal-holes-chronnos-figure1.webp
project_image_alt: "A multichannel view of the solar disk with coronal-hole boundaries traced in red."
excerpt: "Trace the Sun's gateways to fast solar wind. CHRONNOS combines EUV images and magnetic maps, detecting 98.1% of large coronal holes in its test sample."
project_summary: "Trace the Sun's gateways to fast solar wind. CHRONNOS combines EUV images and magnetic maps, detecting 98.1% of large coronal holes in its test sample."
---

{% include project-styles.html %}

[Projects](/projects/) / [Solar feature detection](/projects/#solar-feature-detection)

Coronal holes are dark regions where the Sun's magnetic field opens into interplanetary space. Mapping them consistently helps connect the evolving corona to high-speed solar wind and its effects near Earth.

## CHRONNOS: seeing across wavelengths

**Jarolim et al. (2021), Astronomy & Astrophysics.** CHRONNOS combines seven SDO/AIA EUV channels with SDO/HMI magnetograms. A progressively growing neural network learns both the full-disk context and detailed boundaries, helping distinguish coronal holes from dark filaments.

Against independently reviewed labels, it detected **98.1% of 261 large coronal holes** with areas above **1.5 × 10¹⁰ km²** during 2010–2016. Its intersection-over-union was **0.63**. Detections remained consistent from day to day and across changing solar activity, making the method useful for automated solar-cycle studies.

{% include project-figure.html image="/assets/images/projects/coronal-holes-chronnos-figure1.webp" alt="Composite slices of seven EUV channels and a magnetogram, with CHRONNOS coronal-hole outlines in red." caption="Different wavelengths reveal different parts of the same Sun. CHRONNOS combines them to trace coronal holes while rejecting filament channels that also look dark in EUV." source_url="https://arxiv.org/abs/2104.14313" source_label="Figure 1 · Jarolim et al. (2021), author manuscript" %}

[Read the paper](https://doi.org/10.1051/0004-6361/202140640) · [Open manuscript](https://arxiv.org/abs/2104.14313) · [CHRONNOS code](https://github.com/RobertJaro/MultiChannelCHDetection)

## Testing detections with the community

CHRONNOS also contributes to community validation. A [nine-method comparison](https://doi.org/10.3847/1538-4357/abf2c8) showed that boundary choices can change inferred coronal-hole properties by factors of up to 4.5 in a single case. The subsequent [community benchmark](https://doi.org/10.3847/1538-4365/ad1408) provides 29 challenging observations and results from 14 established schemes, enabling shared tests of true coronal-hole detection and false detections of filaments.

[Explore the benchmark dataset](https://figshare.com/articles/dataset/Coronal_Hole_Detection_Comparison_Dataset/23997993) · [Solar filament detection](/projects/solar-filaments/)
