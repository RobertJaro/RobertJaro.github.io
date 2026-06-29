---
title: "Multi-Height Magnetic Fields"
permalink: /projects/multi-height-magnetic-fields/
---

Part of [Magnetic Field Simulations](/projects/).

This project extends physics-informed magnetic-field extrapolations by incorporating magnetic measurements from multiple atmospheric heights. Standard nonlinear force-free extrapolations are usually constrained only by photospheric vector magnetograms, even though the force-free assumption is more appropriate higher in the solar atmosphere. Multi-height measurements add chromospheric information that can better constrain the coronal magnetic topology.

The method builds on the neural force-free extrapolation framework by representing the magnetic field as a continuous function of coordinates `(x, y, z)`. In addition to the photospheric boundary condition, the model can include internal magnetic-field constraints from higher layers, such as chromospheric line-of-sight magnetograms. Force-free and divergence-free constraints are evaluated through automatic differentiation, while the observed magnetic fields guide the solution at their respective atmospheric heights.

A key component is a learned height-mapping module. Magnetic measurements formed at constant optical depth do not necessarily correspond to a flat geometrical surface; their formation heights can be corrugated by several megameters. The height-mapping model adjusts the local geometrical height of each observed magnetic surface during optimization, allowing the extrapolation to use multi-height observations while also estimating the corrugation of the measurement layer.

The approach was tested on analytical Low and Lou fields, realistic MURaM simulations, and observations combining SDO/HMI photospheric vector magnetograms with SOLIS/VSM chromospheric Ca II 854.2 nm line-of-sight magnetograms. In both analytical and simulated cases, adding chromospheric magnetic information improved the recovered magnetic field and energy distribution. In the observational example of NOAA AR 11166, the multi-height extrapolation produced a more elevated and strongly twisted flux rope that better agreed with EUV and H-alpha observations.

> Figure placeholder: add primary figure and caption.

## Quick Summary
- Objective: improve coronal magnetic-field extrapolations by adding magnetic constraints from chromospheric heights, where the force-free approximation is more realistic than in the photosphere.
- Method: combine a physics-informed neural force-free extrapolation with a learned height-mapping module that accounts for corrugated formation heights of multi-height magnetograms.
- Key result: chromospheric magnetic-field information improves the recovered coronal topology and magnetic-energy distribution, and observational tests show better agreement with EUV and H-alpha structures.

## Reference

- **Jarolim, R.**, Tremblay, B., Rempel, M., Molnar, M., Veronig, A. M., Thalmann, J. K., Podladchikova, T. (2024). Advancing solar magnetic field extrapolations through multiheight magnetic field measurements. *The Astrophysical Journal Letters*, 963, L21.
