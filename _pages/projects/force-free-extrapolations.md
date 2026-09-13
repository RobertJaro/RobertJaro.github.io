---
title: "Force-Free Extrapolations"
permalink: /projects/force-free-extrapolations/
project_category: magnetic-field-simulations
project_order: 1
project_image: /assets/images/projects/force-free-extrapolations-card.webp
project_image_alt: "Reconstructed magnetic field lines above the flare-producing active region NOAA 11158"
excerpt: "Reconstruct the Sun's invisible magnetic architecture with physics-informed neural networks. NF2 modeled five days of active-region evolution in under 12 hours and connected magnetic-energy release to observed flares."
project_summary: "Reconstruct the Sun's invisible magnetic architecture with physics-informed neural networks. NF2 modeled five days of active-region evolution in under 12 hours and connected magnetic-energy release to observed flares."
---

{% include project-styles.html %}

[Projects](/projects/#magnetic-field-simulations) / Magnetic Field Simulations

**Turn surface magnetic measurements into a three-dimensional view of the energy that powers solar eruptions.** NF2 combines observations with the equations of a force-free magnetic field to reconstruct the solar corona.

## Following an active region faster than it evolves

In our **2023 Nature Astronomy study**, NF2 reconstructed five days of NOAA active region 11158 at the full 12-minute cadence of SDO/HMI observations in **less than 12 hours of computation**. The modeled loss of free magnetic energy matched the timing and location of observed flares. Reconstructed flux ropes and other magnetic structures also corresponded to features illuminated in extreme-ultraviolet images.

{% include project-figure.html image="/assets/images/projects/force-free-extrapolations-figure-4.webp" alt="NF2 magnetic field lines and corresponding SDO/AIA extreme-ultraviolet images of active region 11158" caption="Magnetic structures reconstructed before the eruption become visible in EUV emission as the event unfolds. Matching colored outlines identify the same structures in the model and observations." source_url="https://www.nature.com/articles/s41550-023-02030-9/figures/4" source_label="Figure 4 · Jarolim et al. (2023), Nature Astronomy" %}

## How it works

A neural network represents the magnetic field continuously throughout space. Training balances the observed surface field against the force-free and divergence-free equations; successive observations reuse the previous solution to follow the evolving corona efficiently. Analytical benchmarks and comparisons of magnetic energy, helicity, and EUV structures test the reconstruction.

[**Read the paper: Probing the solar coronal magnetic field with physics-informed neural networks**](https://doi.org/10.1038/s41550-023-02030-9) · [NF2 code](https://github.com/RobertJaro/NF2) · [Documentation](https://nf2.readthedocs.io/) · [Research data](https://doi.org/10.6084/m9.figshare.21983486)

Continue with [multi-height magnetic fields](/projects/multi-height-magnetic-fields/), [event studies](/projects/event-studies/), or [global magnetic fields](/projects/global-magnetic-fields/).
