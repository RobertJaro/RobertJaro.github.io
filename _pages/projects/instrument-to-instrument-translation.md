---
title: "Instrument-to-Instrument Translation"
permalink: /projects/instrument-to-instrument-translation/
project_category: image-enhancement
project_order: 1
project_image: /assets/images/projects/instrument-to-instrument-translation-figure5.png
project_image_alt: "Original HMI solar observations, ITI enhancements, and high-resolution Hinode reference images."
excerpt: "Give decades of solar observations a common view. ITI connects 24 years of spacecraft data, sharpens solar images, and brings Solar Orbiter onto the SDO calibration scale."
project_summary: "Give decades of solar observations a common view. ITI connects 24 years of spacecraft data, sharpens solar images, and brings Solar Orbiter onto the SDO calibration scale."
---

{% include project-styles.html %}

[Projects](/projects/) / [Image enhancement](/projects/#image-enhancement)

Better telescopes can improve our view of the past. Instrument-to-Instrument Translation (ITI) learns how different observatories see the Sun, making their images easier to combine across missions, decades, and viewing angles.

## A common language for solar telescopes

**Jarolim et al. (2025), Nature Communications.** ITI uses unpaired generative adversarial networks, so training does not require matching observations from the same place and time. The framework demonstrated four applications: a homogeneous **24-year record** of EUV images and magnetograms; sharper full-disk continuum images; mitigation of atmospheric degradation in ground-based Hα images; and estimates of unsigned far-side magnetic fields from EUV observations.

Comparisons with simultaneous Hinode observations show improved agreement for reconstructed sunspot and granulation structure. The finest inferred detail remains an estimate: some small features differ from the reference, and synthesized far-side magnetic maps are proxies for the unsigned field.

{% include project-figure.html image="/assets/images/projects/instrument-to-instrument-translation-figure5.png" alt="HMI images before and after ITI enhancement, alongside Hinode images and reconstruction error maps." caption="ITI brings out sunspot filaments and granulation in HMI observations. Independent Hinode images test which fine structures the translation recovers." source_url="https://www.nature.com/articles/s41467-025-58391-4/figures/5" source_label="Figure 5 · Jarolim et al. (2025)" %}

[Read the paper](https://doi.org/10.1038/s41467-025-58391-4) · [Code and trained models](https://github.com/RobertJaro/InstrumentToInstrument) · [Documentation](https://iti-documentation.readthedocs.io/)

Figure reproduced unchanged under [CC BY-NC-ND 4.0](https://creativecommons.org/licenses/by-nc-nd/4.0/).

## Connecting Solar Orbiter and SDO

**Schirninger et al. (2025), Astronomy & Astrophysics.** An extension calibrates Solar Orbiter/EUI Full Sun Imager observations to SDO/AIA in the 174/171 Å and 304 Å channels. It handles Solar Orbiter's changing distance and viewpoint, producing light curves that agree better with AIA than the baseline calibration and images with substantially improved perceptual similarity.

This opens a route to consistent EUV observations from multiple sides of the Sun, supporting solar-cycle research and studies of structures beyond Earth's view.

{% include project-figure.html image="/assets/images/projects/instrument-to-instrument-translation-eui-figure3.webp" alt="EUI, ITI-calibrated EUI, and AIA observations in two EUV channels, with close-ups of active regions." caption="Solar Orbiter's original calibration, ITI translation, and the SDO reference on 20 March 2024. The translation aligns both full-disk appearance and active-region detail." source_url="https://arxiv.org/abs/2509.16383" source_label="Figure 3 · Schirninger et al. (2025), author manuscript" %}

[Read the paper](https://doi.org/10.1051/0004-6361/202556401) · [Open manuscript](https://arxiv.org/abs/2509.16383) · [Code](https://github.com/spaceml-org/InstrumentToInstrument)

Related: [Image quality assessment](/projects/image-quality-assessment/) · [Ground-based image reconstruction](/projects/neural-field-blind-deconvolution/).
