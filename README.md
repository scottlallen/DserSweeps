# partialS/HIC Analysis Pipeline
This repository contains the code used for the analysis described in our manuscript. The entire analysis is contained within a single R Markdown (.rmd) file, which is structured as outlined below.

## Table of Contents

### 1. Mapping and Variant Discovery
- Map DsGRP
- GATK genotyping
- Filtering
- Masking
- Phasing

### 2. Haplotype Phasing
- Phase haplotypes
- Synthetic inbreeding

### 3. Generate Empirical Feature Vectors

### 4. Train and predict under constant Ne demography
- Generate training data
- Generate test data
- Run training
- Test on self-new data
- Predict on empirical data

### 5. Demography Analysis (Stairway Plot 2)
- Estimate SFS
- Predict demography
- **Figure 1.**

### 6. Train and predict under Stairway Plot 2 (median) demography
- Generate training data
- Generate test data
- Run training
- Test on self-new data
- Predict on empirical data

### 7. Train and predict under Stairway Plot 2 (2.5th quantile) demography
- Generate training data
- Generate test data
- Run training
- Test on self-new data
- Predict on empirical data

### 8. Train and predict under Stairway Plot 2 (97.5th quantile) demography
- Generate training data
- Generate test data
- Run training
- Test on self-new data
- Predict on empirical data

### 9. Test on mismatched demography

### 10. Figure 2 ROC sweep vs other

### 11. Figure 3 Confusion matrix analysis

### 12. Figure 4 Confusion matrix analsyis (focus on Neutral)

### 13. Figure 5 SP2 median confusion matrix

### 14. Figure 6 Pie and Bar cart for partialS/HIC analysis for * D. serrata *

### 15. Figure 7 Deleterious enrichment of sweep regions

### 16. Empirical prediction statistics

### 17. GO term enrichment

