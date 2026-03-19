---
# Front Matter
layout: default
title: ISMIP7 2026
---

## Antarctic mult-century sea level contribution after an overshoot of the 2°C Paris target

This page contains material from the poster I presented at the **ISMIP7 meeting** in Copenhagen, March 2026.

---

### Abstract

Tipping elements in the Antarctic ice sheet could lead to irreversible sea level rise over the coming centuries. With global emissions rising, a climate ‘overshoot’ – temporarily exceeding  the Paris 2°C target – appears increasingly likely. Whether an overshoot would cause tipping in Antarctica remains unclear. We explore uncertainty in Antarctica’s sea level contribution using the BISICLES ice sheet model, forced by four climate models that have completed an overshoot experiment peaking in 2040. Results are compared with a low-emissions pathway that remains below 2 °C (SSP1-2.6) and a high-emissions pathway with unabated emissions (SSP5-8.5).

---

### Key findings

 - An overshoot of the the 2 °C Paris climate target increases the committed Antarctic sea level contribution by 6.4 ± 5.7 cm relative to meeting the targets.
 - Up to 30 cm additional sea level contribution cannot be ruled out.
 - No evidence of tipping elements triggered during a climate overshoot of this intensity and duration.

---

### Experiment design

We generate a perturbed parameter ensemble, with:
 - 6 perturbed parameters
 - Sobol’ sequence sampling
 - 128-member ensemble
 - 4 forcing GCMs (32 members per GCM)

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

### Climate forcing

The ensemble includes forcing from four CMIP6 models with varying climate sensitivity. There is a wide range of surface mass balance in SSP5-8.5, from positive 2300 values (in MRI) to very negative (in CESM2). See the [supplementary](/projects/ismip7-2026/supplementary) for spatial plots. Overshoot surface mass balance is close to SSP1-2.6, but ocean forcing is slightly higher in some models.

![High-res Plot](/projects/ismip7-2026/figures/smb_anomaly.svg)
*Figure: Antarctic mean surface mass balance anomaly (with 10yr rolling mean) in each scenario and climate model.*

![High-res Plot](/projects/ismip7-2026/figures/thermal_forcing.svg)
*Figure: Ocean thermal forcing anomaly averaged over marine sectors of Antarctica in each scenario and climate model.*

---

### Results
#### Ensemble sea level rise

![High-res Plot](/projects/ismip7-2026/figures/scenario_slc.svg)
*Figure: Sea level contribution in each ensemble member up to 2300 with box-and-whisker plots for each scenario. Dots indicate outliers more than 1.5 x IQR from the median.*

#### The overshoot 'hangover'

![High-res Plot](/projects/ismip7-2026/figures/ssp126_vs_534.svg)
*Figure: Antarctic sea level contribution at 2300 in SSP1-2.6 against that in the overshoot scenario.*

Overshoot sea level contribution is higher than SSP1-2.6 in all members except in MRI-forced runs. A linear relationship between sea level contribution in the overshoot and SSP1-2.6 scenarios suggests that ice sheet tipping elements and non-linear dynamics play a minimal role in the difference.

These results are limited to an overshoot peaking in 2040, but CMIP7 will provide multiple overshoot scenarios of different lengths and intensities.



[Supplementary material](/projects/ismip7-2026/supplementary)

[Back to Projects](/projects)