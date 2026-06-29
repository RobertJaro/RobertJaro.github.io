---
title: "EUV Tomography"
permalink: /projects/euv-tomography/
---

Part of [Tomographic Reconstructions](/projects/).

SuNeRF reconstructs the three-dimensional structure of the solar EUV corona from multi-viewpoint observations. The project addresses the central difficulty of EUV imaging: the corona is optically thin, so each image pixel contains emission integrated along the line of sight, making the true height and geometry of coronal structures ambiguous in ordinary 2D images.

The method adapts neural radiance fields to solar observations. A neural network represents the corona as a continuous spatiotemporal volume, mapping coordinates `(x, y, z, t)` to wavelength-specific emission and absorption coefficients. Known spacecraft positions define rays through the volume, and a simplified radiative-transfer model integrates emission and absorption along each ray to synthesize the observed EUV intensities.

SuNeRF combines simultaneous and time-sequenced observations from SDO/AIA and STEREO/EUVI. Instrument-to-instrument translation is used to place the STEREO observations into an SDO/AIA-like domain, improving consistency across instruments and wavelengths. By using solar rotation and explicit time dependence, the model can reconstruct a global EUV corona even from a small number of simultaneous viewpoints.

The approach was validated with synthetic EUV images from an MHD simulation and applied to real multi-spacecraft observations. It enables reconstructed viewpoints that are not directly observed, improves polar coronal-hole boundary estimates, provides height profiles of coronal holes and filament channels, and tracks the emission and absorption structure of eruptive events such as the 2012 August 31 filament eruption.

> Figure placeholder: add primary figure and caption.

## Quick Summary
- Objective: recover the 3D geometry and height structure of the EUV corona from limited multi-viewpoint solar observations.
- Method: use a solar neural radiance field that maps `(x, y, z, t)` to EUV emission and absorption, then renders observations by integrating along spacecraft-specific lines of sight.
- Key result: SuNeRF reconstructs global coronal structure, improves views of the solar poles, enables height estimates for coronal holes, filaments, and eruptions, and produces realistic novel viewpoints from SDO/STEREO observations.

## Reference

- **Jarolim, R.**, Tremblay, B., Muñoz-Jaramillo, A., Bintsi, K. M., Jungbluth, A., Santos, M., Vourlidas, A., Mason, J., Sundaresan, S., Downs, C., Caplan, R. (2024). SuNeRF: 3D reconstruction of the solar EUV corona using neural radiance fields. *The Astrophysical Journal Letters*, 961, L31.
