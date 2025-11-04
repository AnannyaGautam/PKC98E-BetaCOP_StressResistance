# PKC98E-BetaCOP_StressResistance
This repository contains data and R code for my Honours thesis on how PKC98E and β′COP influence lipid metabolism, stress resistance, and ageing in Drosophila melanogaster. Experiments combine RNAi knockdowns with diet conditioning (5% vs 20% sucrose), survival and activity assays, fecundity counts, food intake, TAG quantification, and qPCR validation.

## Where are the R scripts?
Each major data section contains its own analysis script(s). Open the script within that section to reproduce cleaning, models, and figures for that dataset.

Genotype coding (LAB-ID)

Raw files use LAB-ID for Genotype. Scripts map these to readable labels during analysis.

LAB-ID/Genotype/Notes
1007/ Control (w1118 EV)/ KK library control
1008/ Control (w1118)/ GD library control
1477/	PKC98E RNAi/	VDRC KK
1491/	β′COP RNAi/	VDRC GD
7791/	(double KD)	Double knockdown

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
