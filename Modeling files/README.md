# Modeling Files

This directory contains the model, input data, and supporting configuration files used for the model analysis.

## Contents Overview

| File | Description |
|------|--------------|
| **X8_main_full.out** | Results from the initial model calibration using data through 2020. This file contains the calibrated parameter set used as the baseline for further analysis. |
| **X8_main_sample_frac.tab** | Contains MCMC posterior samples collected after the burn-in period. These point samples were generated during the secondary MCMC calibration and form the basis for the sensitivity analysis. |
| **sens_cont.vsc** | Sensitivity control file specifying which parameters and outputs are included in the sensitivity runs. |
| **ProjEndVals_pessimistic.cin** | Input configuration specifying the “pessimistic” scenario assumptions used during the sensitivity analysis. |
| **plot.lst** | A list file that stores the set of model outputs saved during sensitivity analysis runs. |
| **OSM_Master.vgd** | Custom visualization file that defines display graphs for the Vensim model. |
| **OSM_Master_CURRENT.mdl** | The main system dynamics model file. This is the working version of the calibrated model. |
| **inputtimeseries.vdfx**, **monthlytimeseries.vdfx**, **validationtimeseries.vdfx**, **YearSubs.vdfx** | Time series data used for model calibration. These datasets can be reused for re-calibration or extended analysis. |
| **ProjEndVals_pessimistic** | Configuration file defining the parameter settings for the pessimistic scenario used in sensitivity analysis. |

---

## Workflow Summary

1. **Calibration (Initial)**  
   - The base calibration was performed using data up to 2020.  
   - The calibrated outputs are stored in `X8_main_full.out`.

2. **MCMC Calibration**  
   - A Markov Chain Monte Carlo (MCMC) calibration process was conducted to refine the parameter estimates.  
   - After the burn-in period, posterior samples were saved to `X8_main_sample_frac.tab`.

3. **Sensitivity Analysis**  
   - The MCMC sample points were used as inputs for a sensitivity run.  
   - Sensitivity configurations are defined in `sens_cont.vsc`, and results are recorded based on the specifications in `plot.lst`.  
   - The scenario file `ProjEndVals_pessimistic` defines the external conditions for this run.  
   - **Model outputs from the MCMC-based sensitivity analysis are provided in the “Analysis and Output Files” directory.**

---