# Exploratory Transcriptomic Analysis of Inflammatory Patterns in Psoriasis-Associated Adipose Tissue

## Project Overview

This project explores a public RNA-seq dataset of cutaneous adipose tissue to examine how transcriptomic patterns differ across healthy control, lesional psoriasis, and non-lesional psoriasis samples. The analysis focuses on sample grouping, exploratory gene expression analysis, dimensionality reduction, and visualisation of inflammatory transcriptomic patterns in psoriasis-associated adipose tissue.

## Research Question

How do transcriptomic patterns differ between healthy control, lesional psoriasis, and non-lesional psoriasis adipose tissue samples?

## Dataset

This project uses the public GEO dataset **GSE287022**, which contains RNA-seq data from cutaneous adipose tissue samples collected from healthy controls and psoriasis patients.

For this exploratory analysis, samples were restricted to:
- Healthy control adipose tissue
- Baseline non-lesional psoriasis adipose tissue
- Baseline lesional psoriasis adipose tissue

This filtering was done to avoid confounding from treatment exposure and follow-up timepoints.

## Methods

- Loaded and inspected the raw counts matrix and GEO series matrix metadata
- Extracted and cleaned sample metadata from the series matrix file
- Defined biologically meaningful comparison groups (Healthy, NonLesional, Lesional)
- Matched metadata rows to count-matrix sample columns
- Log-transformed the RNA-seq counts for exploratory analysis
- Identified the top most variable genes across selected samples
- Performed PCA to visualise transcriptomic variation across groups
- Generated heatmaps of top variable genes across samples and by group average
- Mapped Ensembl gene identifiers to readable gene symbols

## Key Findings

- The selected adipose tissue samples showed clear transcriptomic variability across healthy control, non-lesional psoriasis, and lesional psoriasis groups.
- PCA captured most of the overall variation within the first two components, suggesting that major expression differences were reflected in the reduced-dimensional view.
- The grouped heatmap showed that several highly variable genes differed in their average expression across the three groups, pointing towards meaningful biological differences in the tissue states.
- Non-lesional and lesional psoriasis-associated adipose tissue did not appear transcriptomically identical, which suggests that even tissue not visibly lesional may still carry distinct molecular changes.
- Overall, this project helped me understand how public RNA-seq data can be organised, filtered, transformed, and visualised to explore transcriptomic patterns in a clinically relevant disease context.

## Tools Used

- Python
- pandas
- NumPy
- matplotlib
- seaborn
- scikit-learn
- mygene
- Google Colab

## Files

- `psoriasis_adipose_transcriptomics.ipynb` — main notebook containing the full analysis
- `GSE287022_raw_counts_per_gene.csv` — raw gene count matrix
- `GSE287022_series_matrix.txt` — GEO series matrix used for metadata extraction

## Conclusion

This project introduced me to the structure and interpretation of public RNA-seq data and helped me understand how transcriptomic analysis can be used to explore biologically meaningful differences across disease-related tissue states.
