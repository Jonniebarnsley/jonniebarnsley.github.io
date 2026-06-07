---
# Front Matter
layout: default
title: AGU-Chapman 2026
---

## Antarctic mult-century sea level contribution after an overshoot of the 2°C Paris target

This page contains material from my poster at the **AGU Chapman conference on Sea Level Rise** in Montreal, June 2026.

---

### Abstract

Tipping elements in the Antarctic ice sheet could lead to irreversible sea level rise over the coming centuries. With global emissions rising, a climate ‘overshoot’ – temporarily exceeding  the Paris 2°C target – appears increasingly likely. Whether an overshoot would cause tipping in Antarctica remains unclear. We explore uncertainty in Antarctica’s sea level contribution using the BISICLES ice sheet model, forced by four climate models that have completed an overshoot experiment peaking in 2040. Results are compared with a low-emissions pathway that remains below 2 °C (SSP1-2.6) and a high-emissions pathway with unabated emissions (SSP5-8.5).

---

### Key findings

 - An overshoot of the the 2 °C Paris climate target increases the committed Antarctic sea level contribution by 6.9 ± 7.1 cm relative to meeting the targets.
 - Up to 38 cm additional sea level contribution cannot be ruled out.
 - No evidence of tipping elements triggered during a climate overshoot of this intensity and duration.

---

### Experiment design

We generate a perturbed parameter ensemble, with:
 - 6 perturbed parameters
 - Sobol’ sequence sampling
 - 128-member ensemble
 - 4 forcing GCMs (32 members per GCM)
 We emulate BISICLES using Gaussian processes and calibrate to IMBIE Antarctic mass balance 2007-2021.

| Parameter | Long name                | Component        |
|----------|--------------------------|------------------|
| α_φ      | φ-regularisation*        | Initial state    |
| n        | Glen’s exponent          | Rheology         |
| m        | Friction exponent        | Sliding          |
| u₀       | Fast sliding speed       | Sliding          |
| γ        | Basal melt sensitivity   | Sub-shelf melt   |
| UMV      | Upper mantle viscosity   | GIA              |

*\*φ is a spatially varying parameter that represents macroscopic damage and is derived during initialisation via an inverse problem.*

---

### Results
#### Ensemble sea level rise

![High-res Plot](/projects/agu-2026/figures/calibrated_projections.svg)
*Figure: Calibrated Antarctic sea level contribution through 2300. Light / Dark shaded areas represent 5-95% and 17-83% uncertainty ranges, respectively. Boxes show [5, 17, 50, 83, 95]th percentiles per forcing GCM and scenario.*

#### The overshoot 'hangover'

![High-res Plot](/projects/ismip7-2026/figures/ssp126_vs_534.svg)
*Figure: Antarctic sea level contribution at 2300 in SSP1-2.6 against that in the overshoot scenario.*

Overshoot sea level contribution is higher than SSP1-2.6 in all members except in MRI-forced runs. A linear relationship between sea level contribution in the overshoot and SSP1-2.6 scenarios suggests that ice sheet tipping elements and non-linear dynamics play a minimal role in the difference.

These results are limited to an overshoot peaking in 2040, but CMIP7 will provide multiple overshoot scenarios of different lengths and intensities.

#### Sources of uncertainty

 - Uncertainty in the climate forcing dominates in the first 50 years but is rapidly overtaken by uncertainty in ice shelf basal melt.
 - Uncertainty in certain dynamical parameters (n, m) is significant by 2300, but only under high forcing.
 - Sensitivity to the ice sheet initial state is initially high, but decays over time.

![High-res Plot](/projects/agu-2026/figures/sobol_ssp126.svg)

![High-res Plot](/projects/agu-2026/figures/sobol_ssp585.svg)

---

[Supplementary material](/projects/agu-2026/supplementary)

[Back to Projects](/projects)