---
title: "Milne Eddington Inversions with Physics-Informed Neural Networks"
project_short_title: "Milne–Eddington Inversions"
permalink: /projects/milne-eddington-inversions/
project_category: spectropolarimetric-inversions
project_order: 1
project_image: /assets/images/projects/milne-eddington-inversions-thumb.jpg
project_image_alt: "Solar magnetic field maps inferred from Hinode observations with PINN ME."
excerpt: "Recover solar magnetic structure from noisy polarized light. PINN ME couples space and time to suppress noise and reveal coherent magnetic features in Hinode observations."
project_summary: "Recover solar magnetic structure from noisy polarized light. PINN ME couples space and time to suppress noise and reveal coherent magnetic features in Hinode observations."
---

{% include project-styles.html %}

[← Spectropolarimetric inversions](/projects/#spectropolarimetric-inversions)

**PINN ME extracts solar magnetic fields from polarized spectral lines**, using a continuous neural representation to connect neighboring pixels and time steps.

## Clearer magnetic structure · 2025

The network represents atmospheric parameters and passes them through a differentiable Milne-Eddington model to reproduce observed Stokes profiles. Including the instrumental point-spread function accounts for optical blur. In Hinode/SOT-SP observations, the resulting maps show coherent quiet-Sun magnetic elements, smoother field azimuths, and finer penumbral structure than the standard MERLIN comparison. This observational comparison is qualitative because the true magnetic field is unknown. [Read the paper](https://doi.org/10.3847/2041-8213/add342).

{% include project-figure.html image="/assets/images/projects/milne-eddington-inversions-hinode.jpg" alt="PINN ME and MERLIN inversions of Hinode observations, comparing magnetic field components and azimuth in a sunspot and surrounding quiet Sun." caption="Hinode observations reveal coherent weak-field features and detailed penumbral structure. The full maps and enlarged regions compare PINN ME with the standard MERLIN inversions." source_url="https://arxiv.org/html/2502.13924v1#S3.F6" source_label="Figure 6 · Jarolim et al. (2025) · CC BY 4.0" %}

## Resisting noise

Analytical time-series tests show that **temporal coupling strongly reduces noise-driven errors**, especially where polarization signals are weak. Radiative-MHD tests provide a more realistic benchmark. The neural representation also makes extended, coupled inversions memory efficient. The current model retains the Milne-Eddington approximation, so it does not resolve atmospheric gradients with height.

{% include project-figure.html image="/assets/images/projects/milne-eddington-inversions-noise.jpg" alt="Noise benchmark comparing magnetic-field inversions with and without temporal coupling and point-spread-function correction." caption="A controlled benchmark exposes the benefit of temporal information: PINN ME recovers coherent magnetic patterns even as noise degrades the input spectra." source_url="https://arxiv.org/html/2502.13924v1#S2.F3" source_label="Figure 3 · Jarolim et al. (2025) · CC BY 4.0" %}

## Paper and code

- Jarolim, R., Molnar, M. E., Tremblay, B., Centeno, R., and Rempel, M. (2025). [PINN ME: A Physics-informed Neural Network Framework for Accurate Milne-Eddington Inversions of Solar Magnetic Fields](https://doi.org/10.3847/2041-8213/add342). *The Astrophysical Journal Letters*, 985, L7. [Open manuscript](https://arxiv.org/abs/2502.13924).
- [PINN ME source code, installation, and Hinode example](https://github.com/RobertJaro/pinn-me).
