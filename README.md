# partialS/HIC Analysis Pipeline
This repository contains the code used for the analysis described in **our manuscript**. The entire analysis is contained within a single R Markdown (.rmd) file, which is structured as outlined below.

## Link to Published Manuscript
Link to the published manuscript will be added here once available.

## Outline of major R Markdown sections
### 1. Mapping and Variant Discovery
### 2. Haplotype Phasing
### 3. Generate Empirical Feature Vectors
### 4. Train and predict under constant Ne demography
### 5. Demography Analysis (Stairway Plot 2)
### 6. Train and predict under Stairway Plot 2 (median) demography
### 7. Train and predict under Stairway Plot 2 (2.5th quantile) demography
### 8. Train and predict under Stairway Plot 2 (97.5th quantile) demography
### 9. Test on mismatched demography
### 10. Figure 2 ROC sweep vs other
### 11. Figure 3 Confusion matrix analysis
### 12. Figure 4 Confusion matrix analsyis (focus on Neutral)
### 13. Figure 5 SP2 median confusion matrix
### 14. Figure 6 Pie and Bar cart for partialS/HIC analysis for * D. serrata *
### 15. Figure 7 Deleterious enrichment of sweep regions
### 16. Empirical prediction statistics
### 17. GO term enrichment

## Running the partialS/HIC Analysis Pipeline
This guide provides high-level instructions for running the partialS/HIC analysis as described in **the manuscript**. The analysis is contained within a single R Markdown (.rmd) file.

## Prerequisites
Much of the required software was installed via [conda](https://docs.anaconda.com/miniconda/miniconda-install/), but use of this method is optional. Ensure that you have the following software and libraries installed:

### Software
- BWA for mapping
- GATK for variant discovery
- SHAPEIT for haplotype phasing
- Stairway Plot 2 for demography prediction
- R and RStudio for running the R Markdown script
- Python 3 for running the Python scripts

### R Packages
- Listed within the .rmd file

### Python Libraries
- numpy
- pandas
- matplotlib
- seaborn
- scikit-learn
- scipy
- pysam
- tensorflow

### Working with the R Markdown Script
- Although R Markdown files can be viewed as plain text files, they are much easier to work with via RStudio [https://posit.co/download/rstudio-desktop/](https://posit.co/download/rstudio-desktop/).

### Steps to Run the Analysis
#### 1. Mapping and Variant Discovery
- Map DsGRP
- Index the reference genome using BWA.
- Align reads to the reference genome.
- GATK Genotyping
- Pre-process data (duplicate removal, base quality score recalibration).
- Perform variant calling using HaplotypeCaller in GVCF mode.
- Combine GVCFs and perform joint genotyping.
- Filter variants and apply masking.
#### 2. Haplotype Phasing
- Phase Haplotypes
- Phase haplotypes using SHAPEIT.
- Synthetic Inbreeding
- Perform synthetic inbreeding to create homozygous regions for easier analysis.
#### 3. Generate Empirical Feature Vectors
- Convert empirical data to feature vectors required for partialS/HIC analysis.
#### 4. Train and Predict under Constant Ne Demography
- Generate Training Data
- Simulate training data based on a constant Ne demography.
- Generate Test Data
- Simulate test data based on the same demography.
- Run Training
- Train the partialS/HIC model using the generated training data.
- Test on Self-new Data
- Evaluate the trained model on a new set of simulated data.
- Predict on Empirical Data
- Apply the trained model to empirical data for sweep classification.
#### 5. Demography Analysis (Stairway Plot 2)
- Estimate SFS
- Estimate site frequency spectrum (SFS) from intergenic regions.
- Predict Demography
- Predict demographic history using Stairway Plot 2.
#### 6. Train and Predict under Stairway Plot 2 (Median) Demography
- Repeat steps in Section 4 using the SP2 median demography.
#### 7. Train and Predict under Stairway Plot 2 (2.5th Quantile) Demography
- Repeat steps in Section 4 using the SP2 2.5th quantile demography.
#### 8. Train and Predict under Stairway Plot 2 (97.5th Quantile) Demography
- Repeat steps in Section 4 using the SP2 97.5th quantile demography.
#### 9. Test on Mismatched Demography
- Train on one demography and test on another to assess robustness.
#### 10. Analyse Results and Generate Figures
- Figure 2: ROC Curve
  - Generate ROC curves for sweep vs. other classifications.
- Figure 3: Confusion Matrix Analysis
  - Generate confusion matrices for different sweep classes.
- Figure 4: Confusion Matrix Analysis (Focus on Neutral)
  - Detailed analysis focusing on the classification of neutral regions.
- Figure 5: SP2 Median Confusion Matrix
  - Confusion matrix for SP2 median demography.
- Figure 6: Pie and Bar Chart for partialS/HIC Analysis for D. serrata
  - Visual representation of sweep classifications.
- Figure 7: Deleterious Enrichment of Sweep Regions
  - Analysis of SNP enrichment in sweep regions.
#### 11. Empirical Prediction Statistics
- Compile and analyze statistics from empirical data predictions.
#### 12. GO Term Enrichment
- Perform GO term enrichment analysis to identify biological processes associated with sweeps.

## Data Accessibility
DOIs or accession numbers for required files will be added here once available.
