---
title: "Global Magnetic Fields"
permalink: /projects/global-magnetic-fields/
project_category: magnetic-field-simulations
project_order: 4
project_image: /assets/images/projects/global-magnetic-fields-card.webp
project_image_alt: "Full-Sun EUV and H-alpha observations beside a global NF2 magnetic-field reconstruction"
excerpt: "Connect active regions, filament channels, and coronal holes in one magnetic model. The global NF2 reconstruction recovers current-carrying filament structures and large-scale open-field regions."
project_summary: "Connect active regions, filament channels, and coronal holes in one magnetic model. The global NF2 reconstruction recovers current-carrying filament structures and large-scale open-field regions."
project_status: "Preprint results"
---

{% include project-styles.html %}

[Projects](/projects/#magnetic-field-simulations) / Magnetic Field Simulations

**Solar magnetic connections extend beyond the edges of a single active region.** Global NF2 carries physics-informed magnetic reconstruction onto a sphere, bringing local energy storage and large-scale coronal connectivity into one model.

## A magnetic view of the whole Sun

The **2026 SOLER preprint** presents a global reconstruction for February 5, 2016, extending from the solar surface to **1.3 solar radii**. Observed filament channels appear as current-carrying magnetic structures, while coronal holes correspond to open-field regions. Integrated current, magnetic-energy, and current-helicity maps reveal where non-potential structures reside and help characterize their magnetic orientation.

{% include project-figure.html image="/assets/images/projects/global-magnetic-fields-figure-15.webp" alt="Solar EUV and H-alpha images, global magnetic field lines, and maps of current density, magnetic energy and current helicity" caption="One global reconstruction links the filament channels seen in EUV and H-alpha to magnetic structures carrying electric currents, and associates observed coronal holes with open-field regions. The lower panels reveal the magnetic properties of the highlighted area." source_url="https://arxiv.org/html/2608.24458v1#S3.F15" source_label="Figure 15 · Dresing et al. (2026), SOLER preprint" %}

A continuous neural representation and a vector-potential formulation let NF2 reconstruct a divergence-free magnetic field across the spherical domain. The public software includes spherical examples and tools for exporting and analyzing the results.

**Status:** the global demonstration is reported in a manuscript under review. It establishes a pre-eruptive magnetic context; a force-free reconstruction does not describe the full dynamics of an eruption.

[**Comprehensive solar eruption analyses enabled by the tools of the SOLER project**](https://arxiv.org/abs/2608.24458) · [NF2 code](https://github.com/RobertJaro/NF2) · [Spherical modeling guide](https://github.com/RobertJaro/NF2/blob/main/docs/spherical.md) · [Example notebook](https://github.com/RobertJaro/NF2/blob/main/examples/notebooks/spherical_hmi.ipynb)

Explore the local foundations in [force-free extrapolations](/projects/force-free-extrapolations/) and [multi-height magnetic fields](/projects/multi-height-magnetic-fields/).
