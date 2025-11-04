# PKC98E-BetaCOP_StressResistance
This repository contains data and R code for my Honours thesis on how PKC98E and β′COP influence lipid metabolism, stress resistance, and ageing in Drosophila melanogaster. Experiments combine RNAi knockdowns with diet conditioning (5% vs 20% sucrose), survival and activity assays, fecundity counts, food intake, TAG quantification, and qPCR validation.

## Where are the R scripts?
Each major data section contains its own analysis script. Open the script within that section to reproduce cleaning, models, and figures for that dataset.

Raw files use LAB-ID for Genotype. some Scripts map these to readable labels during analysis.

pkgs <- c("tidyverse","survival","coxme","emmeans","lme4","readr")
install.packages(setdiff(pkgs, rownames(installed.packages())))

## Data conventions

Genotype columns use LAB-ID; scripts relabel using geno_labs.

Diet is recorded as numeric (5, 20) and converted to factor labels “5%” and “20%”.

For TAG plates, negative concentrations indicate empty wells. These rows are dropped during cleaning and will become NA after log transforms.

Survival models treat individual flies as the unit of analysis and include block/monitor effects where appropriate.

Activity data from DAMS are summed to 5-minute bins.

## Software
R ≥ 4.3

Packages: tidyverse, survival, coxme, emmeans, lme4, broom, gt, patchwork, readr

# Citing and reuse

If you use this code or data, please cite the thesis once available.
