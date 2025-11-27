# Mendelian randomization study of GLP-1R effects on ovarian cancer subtypes mediated by metabolic factors

This repository contains the code for reproducing the Mendelian randomization (MR) and mediation analyses presented in the manuscript:

Mendelian randomization study of GLP-1R effects on ovarian cancer subtypes mediated by metabolic factors

## Study Overview
Our study employed human genetic data to investigate the causal role of GLP-1 receptor (GLP-1R) activity on ovarian cancer risk and its subtypes. We identified that pancreatic GLP-1R expression was associated with a lower risk of endometrioid ovarian cancer (ENOC), an effect partly mediated by changes in body composition and blood metabolites such as linoleic acid.

## Prerequisites

The analyses require R and the following packages:

```r
# Install core MR packages
install.packages("remotes")
remotes::install_github("MRCIEU/TwoSampleMR")
devtools::install_github("mrcieu/ieugwasr")
install.packages("coloc")
```

## Analysis Scripts
The analytical workflow is divided into four core scripts:
1. MR_analysis_for_outcomes.R  
   Performs MR analysis to estimate the causal effect of GLP-1R expression on overall ovarian cancer and its histotypes (HGSOC, LGSOC, MOC, ENOC, CCOC).
2. MR_analysis_for_potential_mediators.R  
   Identifies and validates candidate metabolic mediators (e.g., BMI, waist circumference, linoleic acid) of the GLP-1R to ENOC pathway using two-step MR.
3. LD_check.R  
   Performs linkage disequilibrium (LD) checks to evaluate whether the genetic associations for GLP-1R expression and the outcomes share a common causal variant.
4. Colocalization.R  
   Conducts colocalization analysis to evaluate whether the genetic associations for GLP-1R expression and the outcomes share a common causal variant.

This code repository is permanently archived on Zenodo: https://doi.org/10.5281/zenodo.17734444
        
        
        
        
