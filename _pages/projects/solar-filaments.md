---
title: "Solar Filaments"
permalink: /projects/solar-filaments/
project_category: solar-feature-detection
project_order: 2
project_image: /assets/images/projects/solar-filaments-detection-figure8.webp
project_image_alt: "Solar filaments outlined in red in full-disk H-alpha observations from ChroTel and GONG."
excerpt: "Follow dark solar filaments across telescopes and through time. Semi-supervised detection reaches 92% accuracy and turns Hα archives into measurements of filament evolution."
project_summary: "Follow dark solar filaments across telescopes and through time. Semi-supervised detection reaches 92% accuracy and turns Hα archives into measurements of filament evolution."
---

{% include project-styles.html %}

[Projects](/projects/) / [Solar feature detection](/projects/#solar-feature-detection)

Dark threads crossing the solar disk trace cool plasma suspended in the Sun's magnetic field. Automatically following these filaments connects individual eruptions with the changing pattern of solar activity.

## From telescope images to filament maps

**Diercke et al. (2024), Astronomy & Astrophysics.** A two-stage method first locates filaments with YOLOv5, then uses those detections to train a U-net that traces their pixels. This semi-supervised approach expands a modest manually labeled dataset using the much larger GONG archive.

The resulting detections achieved **92% accuracy** in the reported evaluation. Demonstrations on **ChroTel, GONG, and Kanzelhöhe** show that the approach transfers across Hα instruments and yields measurable filament areas, positions, and orientations.

{% include project-figure.html image="/assets/images/projects/solar-filaments-detection-figure8.webp" alt="ChroTel and GONG observations of the Sun on 30 March 2013, with filament segmentation contours in red." caption="The same filaments emerge from two observatories. Red contours show automated pixel-level detections in ChroTel and GONG images." source_url="https://arxiv.org/abs/2402.15407" source_label="Figure 8 · Diercke et al. (2024), author manuscript" %}

## Following change from hours to a solar cycle

Applied to a giant filament on 2 September 2014, the segmentation tracks its changing area through eruption. Applied across **GONG observations from 2010–2021**, it recovers the poleward migration of filaments during Solar Cycle 24, demonstrating how automated measurements connect local evolution with global solar magnetism.

{% include project-figure.html image="/assets/images/projects/solar-filaments-eruption-figure13.webp" alt="Five views of an evolving filament and a time series of its segmented area as it erupts." caption="From images to an evolution curve: the detected filament area changes as the structure approaches eruption. The vertical red line marks eruption onset." source_url="https://arxiv.org/abs/2402.15407" source_label="Figure 13 · Diercke et al. (2024), author manuscript" %}

[Read the paper](https://doi.org/10.1051/0004-6361/202348314) · [Open manuscript](https://arxiv.org/abs/2402.15407) · [Segmentation code](https://github.com/adiercke/DeepFilamentSegmentation)

Figures: Diercke et al., [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/); extracted from the manuscript without changes to the plotted content.

Explore the magnetic structures behind filaments in [multi-height magnetic fields](/projects/multi-height-magnetic-fields/) and [solar event studies](/projects/event-studies/).
