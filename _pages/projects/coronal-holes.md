---
title: "Coronal Holes"
permalink: /projects/coronal-holes/
---

Part of [Solar Feature Detection](/projects/).

CHRONNOS is a deep learning framework for automated coronal hole detection in full-disk solar observations. Coronal holes are dark regions in extreme-ultraviolet and soft X-ray images associated with open magnetic-field structures and high-speed solar-wind streams, making reliable boundary detection important for solar-cycle studies and space-weather forecasting.

The method uses a convolutional neural network to segment coronal holes from multi-channel SDO observations. The input combines the seven EUV channels from SDO/AIA with line-of-sight magnetograms from SDO/HMI, allowing the network to use chromospheric, coronal, and photospheric magnetic-field information simultaneously. This multi-spectral view helps distinguish true coronal holes from other dark structures such as filaments.

The primary model, Coronal Hole RecOgnition Neural Network Over multi-Spectral-data (CHRONNOS), uses a progressively growing encoder-decoder architecture. Training starts at low spatial resolution and progressively adds higher-resolution layers, which improves efficiency while preserving both global context across the solar disk and detailed boundary information.

The model was evaluated against an independent manually curated test set across solar cycle 24. It achieved an intersection-over-union of 0.63, correctly detected 98.1% of large coronal holes in the evaluated sample, and classified 97.5% of pixels on average. The detections were temporally smooth over days to weeks and showed the expected anti-correlation between total coronal-hole area and sunspot number over the solar cycle.

> Figure placeholder: add primary figure and caption.

## Quick Summary
- Objective: provide reliable, fully automatic, real-time coronal hole segmentation across different phases of the solar cycle.
- Method: train a progressively growing convolutional neural network on seven SDO/AIA EUV channels and SDO/HMI line-of-sight magnetograms to produce full-disk coronal hole masks.
- Key result: CHRONNOS delivers temporally consistent coronal hole detections, correctly identifies 98.1% of large coronal holes in the test interval, and reduces false detections from filament-like dark structures by combining multi-channel information.

## Reference

- **Jarolim, R.**, Veronig, A. M., Hofmeister, S., Heinemann, S. G., Temmer, M., Podladchikova, T., Dissauer, K. (2021). Multi-channel coronal hole detection with convolutional neural networks. *Astronomy & Astrophysics*, 652, A13.
