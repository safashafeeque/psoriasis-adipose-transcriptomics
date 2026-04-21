# Exploratory Transcriptomic Analysis of Psoriasis-Associated Adipose Tissue

## Project Overview

This was a guided exploratory project completed as part of my learning process in bioinformatics and transcriptomic data analysis. The aim was to understand how public RNA-seq data can be organised, filtered, and visualised in Python in a biologically meaningful way.

## Research Question

How do gene expression patterns differ between healthy control, lesional psoriasis, and non-lesional psoriasis adipose tissue samples?

## Dataset

This project uses the public GEO dataset **GSE287022**, which contains RNA-seq data from cutaneous adipose tissue samples collected from healthy controls and psoriasis patients.

For this exploratory analysis, I focused only on:

- Healthy control adipose tissue
- Baseline non-lesional psoriasis adipose tissue
- Baseline lesional psoriasis adipose tissue

These groups were selected to keep the comparison more focused and to avoid the added effect of treatment exposure or later follow-up timepoints.

## Methods

- Loaded and inspected the raw counts file and GEO series matrix metadata
- Extracted and cleaned sample metadata from the series matrix file
- Defined comparison groups based on condition, tissue type, and timepoint
- Matched the metadata to the sample columns in the count matrix
- Log-transformed the RNA-seq count data for exploratory analysis
- Identified the most variable genes across the selected samples
- Used PCA to explore overall variation across the sample groups
- Created heatmaps to visualise gene expression patterns across samples and by group average
- Mapped Ensembl gene IDs to gene symbols for easier interpretation

## Key Findings

- The selected adipose tissue samples showed noticeable transcriptomic variation across healthy, non-lesional, and lesional groups.
- PCA suggested that a large part of the overall variation could be seen within the first two components.
- The heatmaps showed that several highly variable genes differed across the three groups in their expression patterns.
- Non-lesional and lesional psoriasis-associated adipose tissue did not appear completely identical at the transcriptomic level.
- Overall, this project helped me understand how public RNA-seq data can be prepared and explored to study disease-related expression patterns.

## Concepts Explored

- **RNA-seq count data**: Raw gene expression data showing how many sequencing reads were assigned to each gene.
- **Metadata**: Information about the samples, such as condition, tissue type, and timepoint, which helps organise the analysis properly.
- **Series matrix file**: A GEO text file that contains sample-level metadata and is useful for understanding how samples should be grouped.
- **Count matrix**: A table where rows represent genes and columns represent samples.
- **Log transformation**: A way of transforming count data to make large differences easier to handle and visualise.
- **Variance**: A measure of how much values differ across samples. In this project, it was used to find the most variable genes.
- **PCA (Principal Component Analysis)**: A method used to reduce high-dimensional data into a smaller number of components so overall patterns can be visualised more easily.
- **Heatmap**: A colour-based plot used to show expression patterns across genes and samples.
- **Sample grouping**: Organising samples into comparison groups based on biological or clinical characteristics.
- **Gene ID to symbol mapping**: Converting Ensembl IDs into more readable gene symbols for easier interpretation.
- **DataFrame filtering**: Selecting only the rows or columns relevant to the analysis.
- **Transpose (`.T`)**: Switching rows and columns in a table, which is useful for steps like PCA and grouped expression analysis.


## Tools Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Mygene
- Google Colab

## Files

- `psoriasis_adipose_transcriptomics.ipynb` — main notebook containing the full analysis
- `GSE287022_raw_counts_per_gene.csv` — raw gene count matrix
- `GSE287022_series_matrix.txt` — GEO series matrix used for metadata extraction

## Conclusion

This project helped me get more familiar with the structure of public RNA-seq data and showed me how transcriptomic patterns can be explored in Python using metadata handling, PCA, heatmaps, and gene annotation.

