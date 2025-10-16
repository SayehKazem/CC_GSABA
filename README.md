# CC_GSABA
The Cerebral Cortical Gene-Set Burden Analysis (CC-GSBA) pipeline, included in the PGC-CNV Package, is designed to investigate the impact of Copy Number Variants (CNVs) on Cognitive Ability using Cerebral Cortical Gene-Set Burden Analysis. This repository contains all the code and data required to reproduce the figures and statistical analyses for the project. 
<p align="center">
 <img src="/CC-GSBA_logo.png" alt="CC-GSBA_logo" width="300"/>
</p>

# Project Title
Mirror effect of genomic deletions and duplications on cognitive ability across the human ecerebral cortex

# Project Workflow
This figure outlines our methodology for associating CNVs with cognitive ability by leveraging gene expression data across cortical regions. The analysis integrates genotypic and phenotypic data from large population cohorts with gene expression data from the Allen Human Brain Atlas (AHBA).

- Gene Assignment: Each gene is mapped to cortical regions where it shows preferential expression (z-score > 0.5). This process is repeated for all genes, resulting in 180 distinct regional gene sets.
- CNV Aggregation: For each individual, we calculate two burden metrics for each cortical region:
- Gene-Set Burden: The count of CNVs overlapping genes within a specific regional gene set.
- Genome Burden: The count of CNVs outside that specific regional gene set, serving as a genome-wide control.
Regression Analysis: A regression model is applied to test for a region-specific association between CNV burden and cognitive ability, while controlling for the genome-wide burden and other covariates.  Cognitive ability (Y) is modeled as a function of the Gene-Set Burden and the Genome Burden. The model also adjusts for standard covariates such as age, sex, and ancestry.

<p align="center">
 <img src="CortexWorkflow_v7.png" alt="CortexWorkflow_v7" width="900"/>
</p>


# Citation
If you use this project or its code in your research, please cite this repository. Your citation helps others discover the project and acknowledges our work.

- **Paper:** Kuldeep Kumar, Sayeh Kazem et al. "Mirror effect of genomic deletions and duplications on cognitive ability across the human cerebral cortex." bioRxiv 2025.01.06.631492; 2025.

# Repository Contents
CC-GSBA script: This is the core pipeline for testing the association between CNVs aggregated in cortex-specific gene sets and cognitive ability. 

# File Types
Python Notebooks (*.ipynb): These notebooks contain the code for the main CC-GSBA pipeline. 

# Usage
1. Clone the repository:

```bash
git clone https://github.com/SayehKazem/CC_GSBA.git
