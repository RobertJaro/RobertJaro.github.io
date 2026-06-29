---
title: "Milne Eddington Inversions with Physics-Informed Neural Networks"
permalink: /projects/milne-eddington-inversions/
---

Part of [Spectropolarimetric Inversions](/projects/).

PINN ME is a physics-informed neural network framework for Milne-Eddington inversions of solar spectropolarimetric observations. The method estimates photospheric magnetic field parameters directly from the observed Stokes profiles while retaining the physical forward model used to synthesize polarized spectral lines.

Instead of inverting each pixel independently, the neural network represents the full parameter space as a continuous function of image coordinates and time. Input coordinates `(t, x, y)` are mapped to Milne-Eddington parameters such as magnetic field strength, inclination, azimuth, Doppler velocity, line damping, and source-function terms. These parameters are passed through a differentiable Milne-Eddington forward model to synthesize Stokes `I, Q, U, V` profiles, and the network is optimized by minimizing the difference between synthesized and observed profiles.

This coordinate-based representation creates an intrinsic spatial and temporal coupling between neighboring measurements. As a result, the inversion can suppress observational noise, preserve coherent magnetic structure, and remain memory efficient for extended fields of view and time series. The framework can also include the instrumental point-spread function during optimization, allowing the inferred magnetic parameter maps to account for optical blurring effects.

The method was validated with analytical test cases, synthetic Stokes profiles from radiative MHD simulations, and Hinode/SOT-SP observations. Compared with standard pixel-wise inversions and established Milne-Eddington tools, PINN ME provides smoother weak-field azimuth estimates, coherent quiet-Sun magnetic elements, and higher-contrast fine structure in sunspot penumbrae while retaining comparable physical consistency.

> Figure placeholder: add primary figure and caption.

## Quick Summary
- Objective: infer reliable solar magnetic field parameters from noisy spectropolarimetric observations under the Milne-Eddington approximation.
- Method: encode the inversion parameter space with a physics-informed neural network that maps `(t, x, y)` coordinates to Milne-Eddington parameters, synthesizes Stokes profiles with a differentiable forward model, and optimizes against observed Stokes `I, Q, U, V`.
- Key result: PINN ME introduces memory-efficient spatial and temporal coupling, mitigates observational noise, supports PSF-aware inversions, and resolves coherent small-scale magnetic structure in synthetic and Hinode/SOT-SP data.

## Reference

- **Jarolim, R.**, Molnar, M. E., Tremblay, B., Centeno, R., Rempel, M. (2025). PINN ME: A physics-informed neural network framework for accurate Milne-Eddington inversions of solar magnetic fields. *The Astrophysical Journal Letters*, 985, L7.
