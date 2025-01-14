# Genome-wide Assessment of Runs of Homozygosity in Parkinson’s Disease

`GP2 ❤️ Open Science 😍`

[![DOI](https://zenodo.org/badge/916770992.svg)](https://doi.org/10.5281/zenodo.14647637)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

**Last Updated:** January 2025

## Summary
This repository contains the code, data workflows, and results associated with the manuscript titled ***"Genome-wide assessment identifies novel runs of homozygosity linked to Parkinson’s disease etiology across diverse ancestral populations."*** The study investigates population-specific patterns of Runs of Homozygosity (ROH) and their potential links to Parkinson’s disease (PD) etiology across nine ancestral groups.

### Data Statement
All data used in this study are from **release 6 GP2 data** (GP2 realease 6, DOI: 10.5281/zenodo.10472143; access-controlled via single-sign-on at [gp2.org](https://gp2.org/)).  

---

## Citation
If you use this repository or find it helpful for your research, please cite the corresponding manuscript:

> **Genome-wide assessment identifies novel runs of homozygosity linked to Parkinson’s disease etiology across diverse ancestral populations.**  
> *[Authors, Year]* (DOI: 10.5281/zenodo.14647637)


---

# Workflow Diagram
*(Figure to be attached.)*  
The workflow diagram outlines the key steps in the analysis pipeline, including data preprocessing, ROH detection, annotation, and statistical testing.

---

# Repository Orientation
- The `analyses/` directory includes all analyses discussed in the manuscript.
- The `figures/` directory includes all figures and supplemental figures referenced in the manuscript *(pending publication)*.
- The `tables/` directory includes all tables and supplemental tables referenced in the manuscript *(pending publication)*.

Within the repository:

1. **analyses/**  
2. **data/**  
   - *(Processed data files used or generated during the analyses.)*  
   - **Processed ROH Results**: Summary statistics and annotated ROH regions for each ancestral group.
3. **results/**  
   - Contains population-specific ROH burden results, statistical significance outputs, and summary tables for manuscript figures/supplementary materials.

---

## Key Analyses
1. **Runs of Homozygosity Detection**  
   - ROH regions were identified for nine ancestral groups (AAC, AFR, AJ, AMR, CAS, EAS, EUR, MDE, SAS) using PLINK’s `--homozyg` function with standardized parameters.
2. **Functional Annotation**  
   - ROH regions were annotated with conservation scores, overlapping genes, and functional genomic features to assess potential impact on PD etiology.
3. **Phenotype Association Testing**  
   - Association tests were conducted between ROH burden and Parkinson’s disease risk, stratified by ancestry.
4. **Statistical Significance**  
   - Ancestry-specific patterns and overlaps of significant ROH regions were identified.  
5. **Results Interpretation**  
   - Significant ROH regions were further mapped to known PD risk loci, genes, and pathways to understand potential disease mechanisms.

---

### Figures and Supplemental Figures
*(Pending publication)*

### Tables and Supplemental Tables
*(Pending publication)*

---

## Analysis Notebooks
*Languages: Python, Bash, and R*

| **Notebook**                | **Description**                                                                                                                                                                                 |
|:---------------------------:|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **00_ROH_calculation.ipynb** | Identifies related individuals, conducts QC on imputed genotype data, detects ROHs using PLINK, finds overlapping ROHs in PD genes, and applies significance testing                                                                 |
| **01_ROH_statistics.ipynb**  | Investigates ROH burden in PD by performing regression, t-tests, and mapping ROH regions to PD-related genes                                                                                                                          |
| **02_ROH_mapping.ipynb**     | Integrates conservation scores to prioritize regions of interest, examines overlaps between ROH regions and known genes, maps ROH regions to functional genomic features, and visualizes spatial distributions across ancestries       |

---

## Software

|            Software            | Version(s)        |                       Resource URL                       |       RRID       |                                       Notes                                        |
|:-----------------------------:|:-----------------:|:--------------------------------------------------------:|:----------------:|:----------------------------------------------------------------------------------:|
| Python Programming Language   | 3.8 and 3.9       | [http://www.python.org/](http://www.python.org/)         | RRID:SCR_008394  | *pandas, numpy, seaborn, matplotlib, statsmodel; used for data wrangling/analyses* |
| R Project for Statistical Computing | 4.2         | [http://www.r-project.org/](http://www.r-project.org/)   | RRID:SCR_001905  | *tidyverse, dplyr, tidyr, ggplot, data.table; used for data wrangling/analyses*     |
| ANNOVAR                       | 2020-06-08        | [http://www.openbioinformatics.org/annovar/](http://www.openbioinformatics.org/annovar/) | RRID:SCR_012821 | *refGene, avsnp150, ljb26_all, gnomad312_genome; used for annotation*              |
| PLINK                         | 1.9 and 2.0       | [http://www.nitrc.org/projects/plink](http://www.nitrc.org/projects/plink)         | RRID:SCR_001757  | *Used for genetic analyses, including ROH detection*                                |

