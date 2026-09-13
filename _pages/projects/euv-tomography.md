---
title: "EUV Tomography"
permalink: /projects/euv-tomography/
project_category: tomographic-reconstructions
project_order: 1
project_image: /assets/images/projects/euv-tomography-thumb.jpg
project_image_alt: "SuNeRF reconstruction of the solar south pole, with the polar coronal hole outlined in red."
excerpt: "See the Sun from new angles. SuNeRF turns SDO and STEREO images into an evolving 3D corona, revealing polar coronal holes and the height structure of solar eruptions."
project_summary: "See the Sun from new angles. SuNeRF turns SDO and STEREO images into an evolving 3D corona, revealing polar coronal holes and the height structure of solar eruptions."
---

{% include project-styles.html %}

[← Tomographic reconstructions](/projects/#tomographic-reconstructions)

SuNeRF brings depth to solar images: its evolving 3D representation lets us inspect the corona from new viewpoints and trace structures above the visible surface.

## Seeing the solar poles · 2024

Combining SDO/AIA and STEREO/EUVI image sequences, **SuNeRF reconstructs the global EUV corona with three simultaneous observing instruments**. The network models emission and absorption throughout space and time, accounting for light integrated along each viewing direction. Reconstructed polar views reveal coronal-hole boundaries that ordinary spherical reprojection distorts. [Read the paper](https://doi.org/10.3847/2041-8213/ad12d2).

{% include project-figure.html image="/assets/images/projects/euv-tomography-poles.jpg" alt="South-pole reconstruction and comparisons of spherical reprojection, SuNeRF images, and uncertainty at increasing solar latitudes." caption="A view over the south pole reveals the coronal hole. Below, SuNeRF preserves coronal structure as the viewpoint moves away from the ecliptic; uncertainty maps identify less constrained regions." source_url="https://arxiv.org/html/2401.16388v1#S3.F3" source_label="Figure 3 · Jarolim et al. (2024) · CC BY 4.0" %}

For the **31 August 2012 filament eruption**, a focused two-viewpoint reconstruction tracks the filament's rise and ejection, distinguishing elevated absorbing plasma from flare ribbons near the surface. These are model-derived height estimates; ensemble uncertainty maps help assess the reconstruction.

{% include project-figure.html image="/assets/images/projects/euv-tomography-eruption.jpg" alt="SuNeRF images, height maps, and emission and absorption slices through the 31 August 2012 solar filament eruption." caption="The eruption gains a third dimension: height maps and evolving atmospheric slices separate the rising filament, its ejection, and the flare emission left behind." source_url="https://arxiv.org/html/2401.16388v1#S3.F5" source_label="Figure 5 · Jarolim et al. (2024) · CC BY 4.0" %}

## Validating unseen viewpoints · 2022

The precursor study tested SuNeRF against simulated EUV images with known ground truth. Trained only on viewpoints near the ecliptic, it reconstructed unseen higher latitudes with **0.3% mean absolute relative error**, versus 3.4% for spherical reprojection. This established the basis for applying the method to real spacecraft observations. [Read the workshop paper](https://arxiv.org/abs/2211.14879).

{% include project-figure.html image="/assets/images/projects/euv-tomography-validation.jpg" alt="Validation of SuNeRF against simulated solar images, showing agreement at unseen high-latitude viewpoints and associated uncertainty maps." caption="The simulation supplies the missing ground truth: reconstructed views closely match the reference corona even far from the training viewpoints near the ecliptic." source_url="https://arxiv.org/abs/2211.14879" source_label="Figure 3 · Bintsi et al. (2022)" %}

## Papers and code

- Jarolim, R., et al. (2024). [SuNeRF: 3D Reconstruction of the Solar EUV Corona Using Neural Radiance Fields](https://doi.org/10.3847/2041-8213/ad12d2). *The Astrophysical Journal Letters*, 961, L31. [Open manuscript](https://arxiv.org/abs/2401.16388).
- Bintsi, K.-M., Jarolim, R., et al. (2022). [SuNeRF: Validation of a 3D Global Reconstruction of the Solar Corona Using Simulated EUV Images](https://arxiv.org/abs/2211.14879). *Machine Learning and the Physical Sciences Workshop, NeurIPS 2022*.
- [SuNeRF source code and example configurations](https://github.com/RobertJaro/SuNeRF).
- Continue into the heliosphere: [white-light CME tomography](/projects/white-light-tomography/).
