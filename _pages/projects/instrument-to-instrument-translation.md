---
title: "Instrument-to-Instrument Translation"
permalink: /projects/instrument-to-instrument-translation/
---

Part of [Image Enhancement](/projects/).

Instrument-to-instrument translation (ITI) uses deep learning to homogenize solar observations across different telescopes, missions, and observing conditions. The goal is to make heterogeneous data sets easier to combine by translating lower-quality or differently calibrated observations into the image domain of a modern reference instrument.

This project addresses a recurring challenge in solar physics: instruments improve over time, but earlier observations do not automatically benefit from better spatial resolution, calibration, or image quality. Differences between instruments can limit long-term solar-cycle studies, multi-mission comparisons, and automated pipelines that expect consistent observables. ITI provides a data-driven way to bridge those gaps without requiring perfectly aligned image pairs.

The framework is based on unpaired image-to-image translation with generative adversarial networks. A pair of generator networks learns translations between low-quality and high-quality image domains, while discriminator networks enforce that generated images match the target domain. Cycle consistency helps preserve the physical content of the input observations, and an additional noise term allows the model to represent diverse degrading effects such as instrumental blur, atmospheric seeing, or calibration differences.

Because the method does not require spatial or temporal overlap between instruments, it can be applied to data sets with different observing periods, cadences, fields of view, or vantage points. The framework was demonstrated on four solar-observation tasks: inter-calibrating SOHO/EIT, STEREO/EUVI, SOHO/MDI, SDO/AIA, and SDO/HMI data; super-resolving SDO/HMI continuum observations toward Hinode/SOT-BFI quality; mitigating atmospheric degradation in Kanzelhöhe H-alpha observations; and estimating far-side unsigned magnetic field information from STEREO/EUVI imagery.

The resulting translations produce perceptually similar high-quality observations and more homogeneous multi-instrument time series. For long-term EUV and magnetogram data, the approach supports consistent calibration across more than two solar cycles. For image enhancement tasks, it improves the visibility of fine solar structure while retaining the limits imposed by the information present in the original data.

> Figure placeholder: add primary figure and caption.

## Quick Summary
- Objective: homogenize solar observations from different instruments and observing conditions so that long-term and multi-mission data sets can be analyzed more consistently.
- Method: train unpaired GAN-based image translation models with cycle consistency to map low-quality or differently calibrated observations into a high-quality target instrument domain without requiring aligned image pairs.
- Key result: ITI enables EUV and magnetogram inter-calibration, continuum-image super-resolution, ground-based H-alpha seeing mitigation, and far-side magnetic-field proxy estimation across heterogeneous solar data sets.

## Reference

- **Jarolim, R.**, Veronig, A. M., Pötzi, W., Podladchikova, T. (2025). A deep learning framework for instrument-to-instrument translation of solar observation data. *Nature Communications*, 16, 3157.
