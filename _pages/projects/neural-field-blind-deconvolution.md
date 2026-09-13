---
title: "Neural Field Blind Deconvolution"
permalink: /projects/neural-field-blind-deconvolution/
project_category: image-enhancement
project_order: 3
project_image: /assets/images/projects/neural-field-blind-deconvolution-dkist-figure8a.webp
project_image_alt: "DKIST sunspot detail compared across original frames, speckle, multiframe blind deconvolution, and NeuralBD reconstructions."
excerpt: "Recover fine solar structure through atmospheric blur. NeuralBD jointly reconstructs the solar image and its blurring functions, with demonstrations on simulations, GREGOR, and DKIST."
project_summary: "Recover fine solar structure through atmospheric blur. NeuralBD jointly reconstructs the solar image and its blurring functions, with demonstrations on simulations, GREGOR, and DKIST."
---

{% include project-styles.html %}

[Projects](/projects/) / [Image enhancement](/projects/#image-enhancement)

Earth's atmosphere blurs even the sharpest solar telescopes. By combining short exposures with the physics of image formation, neural reconstruction methods recover the fine structure hidden across a burst of observations.

## Learning the Sun and the blur together

**Schirninger et al. (2026), Astronomy & Astrophysics.** NeuralBD represents the underlying image as a continuous neural field and simultaneously fits a point-spread function for each exposure. Blurring the reconstructed image with those functions must reproduce the observed burst, tying the reconstruction directly to the measurements.

On the paper's synthetic MURaM test, NeuralBD reached a structural similarity score of **0.96**, compared with **0.57** for the tested multiframe blind-deconvolution configuration and **0.49** for Richardson–Lucy deconvolution. Applications to **GREGOR and DKIST** resolved fine solar features and enabled direct comparisons with established reconstruction methods. These results apply to the tested data and configurations.

{% include project-figure.html image="/assets/images/projects/neural-field-blind-deconvolution-dkist-figure8a.webp" alt="Original DKIST sunspot images and three reconstruction methods, with successively magnified penumbral structures." caption="DKIST sunspot structure across the original burst and three reconstruction methods. The progressively enlarged regions expose differences in the recovered fine detail." source_url="https://arxiv.org/abs/2603.05033" source_label="Figure 8a · Schirninger et al. (2026), author manuscript" %}

[Read the paper](https://doi.org/10.1051/0004-6361/202658932) · [Open manuscript](https://arxiv.org/abs/2603.05033) · [NeuralBD code](https://github.com/Schirni/NeuralBD)

## A hundred frames, one sharp view

**Schirninger et al. (2025), Astronomy & Astrophysics.** The related burst-stacking study extends [ITI](/projects/instrument-to-instrument-translation/) to turn **100 short exposures into one reconstruction in about 0.5 seconds** on the reported GPU setup. Unpaired training uses speckle reconstructions as examples of high-quality images. The method delivers comparable reconstructions and improved perceptual robustness when speckle processing produces artifacts; using the full burst gives the best tested results.

{% include project-figure.html image="/assets/images/projects/neural-field-blind-deconvolution-burst-figure3.webp" alt="Original and ITI-reconstructed G-band solar images showing granulation, bright points, pores, and sunspot structure." caption="Burst stacking recovers granulation, bright points, and sunspot structure from atmospheric blur. Each left-hand image is a single input frame; the right-hand image combines the burst." source_url="https://arxiv.org/abs/2506.04781" source_label="Figure 3 · Schirninger et al. (2025), author manuscript" %}

[Read the paper](https://doi.org/10.1051/0004-6361/202451850) · [Open manuscript](https://arxiv.org/abs/2506.04781) · [Code](https://github.com/spaceml-org/InstrumentToInstrument)

## Ongoing work

*Spatially variant neural blind deconvolution to reconstruct ground-based solar observations* (Schirninger et al., 2026) extends this direction to blur that varies across the field of view. It is listed as **under revision** in the [publication record](/publications/). Results and figures from this follow-up will be added when a public manuscript is available.
