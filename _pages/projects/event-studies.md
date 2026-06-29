---
title: "Event Studies"
permalink: /projects/event-studies/
---

Part of [Magnetic Field Simulations](/projects/).

This project uses time-dependent magnetic-field extrapolations to study flare-productive active regions and eruptive events. The goal is to connect the evolution of the coronal magnetic field with observed flares, coronal mass ejections, and the release of stored magnetic energy.

A recent focus is NOAA active region 13664, the source of the May 2024 extreme geomagnetic storm and one of the most flare-productive active regions of recent decades. The region produced numerous M- and X-class flares, including multiple Earth-directed eruptions that contributed to the strongest geomagnetic storm since 2003.

The study uses NF2 nonlinear force-free extrapolations based on physics-informed neural networks, driven by full-cadence SDO/HMI vector magnetograms. The model series covers 2024 May 5 to May 11 at the native 12 minute HMI cadence. A vector-potential formulation was introduced to obtain intrinsically divergence-free magnetic fields, while the time-series training strategy enables quasi-real-time extrapolations across the active-region evolution.

The analysis tracks magnetic energy, free magnetic energy, current density, squashing factor, and twist number throughout the active region. Decreases in relative free magnetic energy were associated with solar flares in about 90% of significant cases, and all considered X-class flares corresponded to a decrease in relative free magnetic energy. Spatial maps of depleted magnetic energy aligned with EUV brightenings in SDO/AIA observations, connecting modeled energy release to flare ribbons and hot flare plasma.

The X3.9 flare on 2024 May 10 was analyzed in detail. The extrapolations show interacting magnetic domains, a filament channel, overlying loops, and a fan-spine-like configuration. The modeled current-density evolution indicates topological reconfiguration and the formation of a new current channel during the eruption, supporting a magnetic-reconnection interpretation of the event.

> Figure placeholder: add primary figure and caption.

## Quick Summary
- Objective: connect flare and CME activity to the buildup, storage, and release of magnetic energy in complex solar active regions.
- Method: compute high-cadence NF2 nonlinear force-free extrapolation series from SDO/HMI vector magnetograms, using a vector-potential formulation for solenoidal magnetic fields and comparing modeled energy changes with SDO/AIA flare signatures.
- Key result: for AR 13664, all analyzed X-class flares correspond to decreases in relative free magnetic energy, and energy-depletion maps align with EUV flare brightenings and magnetic reconnection signatures.

## Reference

- **Jarolim, R.**, Veronig, A. M., Purkhart, S., Zhang, P., Rempel, M. (2024). Magnetic field evolution of the solar active region 13664. *The Astrophysical Journal Letters*, 976, L12.
