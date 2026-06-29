---
title: "Force-Free Extrapolations"
permalink: /projects/force-free-extrapolations/
---

Part of [Magnetic Field Simulations](/projects/).

This project develops physics-informed neural networks for nonlinear force-free (NLFF) extrapolations of the solar coronal magnetic field. The goal is to infer the three-dimensional coronal magnetic structure from routinely observed photospheric vector magnetograms, where direct measurements of the upper solar atmosphere are usually unavailable.

The method represents the magnetic field as a continuous neural function that maps spatial coordinates `(x, y, z)` to the magnetic-field vector `(Bx, By, Bz)`. At the photospheric boundary, the model is constrained by the observed vector magnetogram. Inside the coronal volume, automatic differentiation is used to evaluate the force-free and divergence-free equations, allowing the neural network to optimize a field that balances the observational boundary data with the physical assumptions of a force-free corona.

This formulation avoids rigid preprocessing of the input magnetogram and instead learns a trade-off between imperfect observations and the imperfect force-free approximation. The resulting neural representation is mesh-free, differentiable, and efficient to update for time series. By initializing each new extrapolation from the previous solution, the method can follow the evolution of an active region at high cadence with substantially reduced computation time.

The approach was validated against analytical Low and Lou force-free fields and applied to the flare-productive active region NOAA 11158. The time-dependent simulation recovered the build-up and depletion of free magnetic energy and magnetic helicity across five days of SDO/HMI observations. The spatial and temporal depletion of free magnetic energy aligned with observed flare activity in SDO/AIA extreme-ultraviolet data, linking the modeled coronal energy release to the observed eruptions.

> Figure placeholder: add primary figure and caption.

## Quick Summary
- Objective: reconstruct the three-dimensional coronal magnetic field from photospheric vector magnetograms and quantify the magnetic energy available for solar eruptions.
- Method: use a physics-informed neural network as a continuous magnetic-field representation, constrained by observed boundary fields and by force-free and divergence-free equations evaluated with automatic differentiation.
- Key result: the method reproduces analytical force-free test cases, enables high-cadence time-series extrapolations, and links the depletion of modeled free magnetic energy in NOAA 11158 to observed flare activity.

## Reference

- **Jarolim, R.**, Thalmann, J. K., Veronig, A. M., Podladchikova, T. (2023). Probing the solar coronal magnetic field with physics-informed neural networks. *Nature Astronomy*, 7, 1171-1179.
