---
# Front Matter
layout: default
title: AGU-Chapman 2026
---

## Antarctic mult-century sea level contribution after an overshoot of the 2°C Paris target

This page contains supplementary material to my poster at the **AGU Chapman conference on Sea Level Rise** in Montreal, June 2026.

### Climate forcing

The ensemble includes forcing from four CMIP6 models with varying climate sensitivity. There is a wide range of surface mass balance in SSP5-8.5, from positive 2300 values (in MRI) to very negative (in CESM2). See the [supplementary](/projects/ismip7-2026/supplementary) from my poster at the *ISMIP7 2026* meeting for spatial plots. Overshoot surface mass balance is close to SSP1-2.6, but ocean forcing is slightly higher in some models.

![High-res Plot](/projects/ismip7-2026/figures/smb_anomaly.svg)
*Figure: Antarctic mean surface mass balance anomaly (with 10yr rolling mean) in each scenario and climate model.*

![High-res Plot](/projects/ismip7-2026/figures/thermal_forcing.svg)
*Figure: Ocean thermal forcing anomaly averaged over 400-800m depth and over marine sectors of Antarctica in each scenario and climate model.*

---

**Comparison with observations**

The West-Antarctic sea level contribution over the observational period is in good agreement with IMBIE 2007-2021. However, the ensemble systematically underestimates East-Antarctic sea level contribution and overestimates Antarctic Peninsula sea level contribution. This is relatively independant of the scenario (which diverge only after 2015), but is highly dependant on the forcing GCM.

![High-res Plot](/projects/agu-2026/figures/WAIS_sle.svg)
*Figure: Sea level contribution from West Antarctica over the observational period (2007-2021), with kernel density estimates broken down by scenario and by forcing GCM. The IMBIE range for the same period is highlighted in red.*

![High-res Plot](/projects/agu-2026/figures/EAIS_sle.svg)
*Figure: Sea level contribution from East Antarctica over the observational period (2007-2021), with kernel density estimates broken down by scenario and by forcing GCM. The IMBIE range for the same period is highlighted in red.*

![High-res Plot](/projects/agu-2026/figures/APIS_sle.svg)
*Figure: Sea level contribution from the Antarctic Peninsula over the observational period (2007-2021), with kernel density estimates broken down by scenario and by forcing GCM. The IMBIE range for the same period is highlighted in red.*

---

**Emulator diagnostics**

We emulate BISICLES using Gaussian Processes for use in the calibration. We emulate sea level contribution from each of the West, East, and Peninsula ice sheets separately and perform a joint calibration against IMBIE regional mass balance. Here, we show that the emulator reproduces BISICLES 2300 sea level contribution from the component ice sheets with good accuracy and an appropriate level of uncertainty.

![High-res Plot](/projects/agu-2026/figures/loo_2300_WAIS.svg)
*Figure: Leave-one-out analysis for the West Antarctic Ice Sheet. BISICLES samples are systematically dropped from the ensemble and then predicted using an emulator trained on all other data. Samples that 'pass' (they fall within the predicted emulator uncertainty) are labelled in blue; samples that fail are labelled in red.*

![High-res Plot](/projects/agu-2026/figures/loo_2300_EAIS.svg)
*Figure: Equivalent plot for the East Antarctic Ice Sheet.*

![High-res Plot](/projects/agu-2026/figures/loo_2300_APIS.svg)
*Figure: Equivalent plot for the Antarctic Peninsula Ice Sheet.*

We also look at the main effects of each perturbed parameter on sea level contribution from the component ice sheets by emulating a sweep of parameter values with all other parameters held at their midpoint. The plots below are shown for CESM2-WACCM in SSP5-8.5, but the main effects are similar (but not exactly the same) for other forcing GCMs and scenarios.

![High-res Plot](/projects/agu-2026/figures/main_effects_2300_WAIS_CESM2-WACCM_ssp585.svg)
*Figure: Parameter sensitivity of sea level contribution from the West Antarctic Ice Sheet over each parameter range. Also shows the form of the relationship between parameter and sea level rise, including saturation effects (e.g. α_φ).*

![High-res Plot](/projects/agu-2026/figures/main_effects_2300_EAIS_CESM2-WACCM_ssp585.svg)
*Figure: Equivalent plot for the East Antarctic Ice Sheet.*

![High-res Plot](/projects/agu-2026/figures/main_effects_2300_APIS_CESM2-WACCM_ssp585.svg)
*Figure: Equivalent plot for the Antarctic Peninsula Ice Sheet.*

---

**Calibration**

IMBIE mass balance is a weak constraint on the BISICLES ensemble due to the short calibration time period (2007-2021) and relatively low ensemble spread. Calibration is performed separately per forcing GCM and then combined using a unform prior over GCMs. This is done to acknowledge that the GCM-dependance of sea level contribution over the short calibration period is dominated by inter-decadal variability and not a true indication of GCM likelihood. All calibration is done against an SSP1-2.6, since a scenario must be chosen for sea level past 2015. However, sea level over the calibration period (and therefore the calibration itself) is mostly inert to the choice of scenario. We show the prior and posterior distributions for each parameter using the MRI GCM forcing below.

![High-res Plot](/projects/agu-2026/figures/posterior_marginals.svg)
*Figure: Posterior marginals for each parameter, assuming MRI forcing.*

Most GCMs are only slightly constrained by the calibration, but the MIROC ensemble members are well-constrained due to a higher ensemble spread across MIROC-forced simulations. The calibration squashes the high sea level MIROC runs associated with high values of the sub-shelf melt sensitivity.

![High-res Plot](/projects/agu-2026/figures/projection_bands.svg)
*Figure: Prior and posterior projections under each scenario and forcing GCM. Also provided is a 'combined GCM' distribution, which assumes a uniform prior over GCMs.*

---

[Back to poster](/projects/agu-2026/main)