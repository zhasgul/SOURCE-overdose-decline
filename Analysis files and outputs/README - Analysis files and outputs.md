# Analysis and Output Files

This directory contains the outputs of the model sensitivity analyses, as well as post-processing and visualization scripts used for result generation and supplementary material preparation.

## Contents Overview

| File | Description |
|------|--------------|
| **Pessimistic2020X8_perdt_simulation_forR.zip** | Compressed archive containing the model output generated under the pessimistic scenario. This includes the results from the MCMC-based sensitivity analysis. |
| **Pessimistic2020X8_perdt_data_forR.xlsx** | Data file corresponding to the simulation outputs. These datasets are imported into R for visualization and further statistical processing. |
| **MCMC output analysis and visualization.Rmd** | R Markdown script used to import the simulation and data files, perform MCMC output analysis, and generate the final figures and summary statistics. |
| **figure1**, **figure2** | High-quality visualizations generated in R based on the MCMC sensitivity outputs and scenario simulations. |
| **Supplement table.xlsx** | Table in supplementary results containing the calculated 95% credible intervals and mean absolute error (MAE) statistics for projection and overdose data comparison. |

---

## Workflow Summary

1. **Model Output Generation**  
   - The pessimistic scenario sensitivity analysis with MCMC samples was executed within the Vensim model.  
   - Results were exported and compressed into `Pessimistic2020X8_perdt_simulation_forR.zip`.

2. **Data Import and Analysis in R**  
   - The model output and corresponding dataset (`Pessimistic2020X8_perdt_data_forR.xlsx`) are imported into R.  
   - The R Markdown script `MCMC output analysis and visualization.Rmd` processes the MCMC sensitivity outputs and generates figures.

---
