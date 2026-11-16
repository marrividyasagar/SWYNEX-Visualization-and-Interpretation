# GSE20966: Gene Expression Data Visualization and Interpretation

## Project Overview

This project focuses on visualizing and interpreting gene expression data from the NCBI Gene Expression Omnibus (GEO) dataset **GSE20966**.

The dataset contains gene expression profiles from beta-cell-enriched tissue samples obtained from individuals with Type 2 Diabetes and non-diabetic controls.

The objective is to explore expression patterns, compare samples, and identify visual trends using Python data visualization techniques.

## Dataset Information

- **Dataset ID:** GSE20966
- **Source:** NCBI Gene Expression Omnibus (GEO)
- **Organism:** Homo sapiens
- **Platform:** GPL1352 – Affymetrix Human X3P Array
- **Total samples:** 20
- **Control samples:** 10
- **Type 2 Diabetes samples:** 10
- **Probe identifiers:** 61,295 per sample

[View the dataset on NCBI GEO](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE20966)

## Tools and Libraries

- Python
- Google Colab
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

## Visualization and Analysis

### 1. Gene Expression Distribution

A boxplot was generated to examine the distribution of expression signals across all 20 samples.

**Interpretation:** The boxplot helps compare the central values, spread, and potential outliers in the samples. It provides an overview of variation in expression signals across the dataset.

### 2. Sample Correlation Heatmap

A correlation heatmap was generated to examine similarities in expression patterns between samples.

**Interpretation:** The heatmap helps identify samples with similar expression profiles and explore whether control and diabetes samples show group-related patterns.

### 3. Principal Component Analysis (PCA)

PCA was performed to reduce the dimensionality of the expression dataset and visualize sample-level variation.

- PC1 explained approximately 12.84% of the variance.
- PC2 explained approximately 9.00% of the variance.
- Together, the first two components explained approximately 21.84% of the variance.

**Interpretation:** The PCA plot showed partial separation between control and diabetes samples. This suggests some differences in their overall expression patterns, although overlap between groups remains.

### 4. Control vs Diabetes Group Comparison

A grouped bar chart was generated to compare mean expression signals for selected highly variable probe identifiers.

**Interpretation:** Most of the selected probes showed higher average signals in the diabetes group, while some showed similar or higher signals in the control group.

The probe `g13544062_3p_at` was excluded from this particular chart because its extreme values made the other bars difficult to compare. The original dataset was not modified.

## Important Data Quality Observation

The processed expression matrix contained negative measurements and some unusually large values. These were not automatically removed or replaced.

The unusual values require further investigation before any decision about data exclusion or correction can be made.

## Scientific Limitations

- The visualizations provide exploratory and descriptive information.
- PCA separation does not establish statistical significance.
- Differences in group averages do not prove differential expression.
- The analysis does not establish a causal relationship between diabetes and gene expression.
- Probe identifiers should not be treated as confirmed gene identities without appropriate annotation.
- Further statistical testing and probe annotation are needed to identify potentially differentially expressed genes.

## Conclusion

The visualization analysis provided an overview of expression signal distributions, sample similarities, and differences between control and Type 2 Diabetes groups.

The PCA plot showed partial separation between the groups, while the grouped bar chart revealed variation in average signals across selected probes.

These findings provide an exploratory understanding of the dataset and can guide further statistical and biological investigation.

## Repository Contents

- `SWYNEX_Data_Cleaning_Basic_Analysis.ipynb` – Python analysis notebook
- `expression_boxplot.png` – Expression distribution
- `correlation_heatmap.png` – Sample correlation heatmap
- `PCA_plot_labeled.png` – PCA visualization
- `group_comparison_clean.png` – Control vs Diabetes comparison
- `cleaned_gene_expression.csv` – Loaded expression matrix
- `sample_statistics.csv` – Sample-level descriptive statistics
- `control_vs_diabetes.csv` – Group comparison results

## Acknowledgement

Dataset obtained from the NCBI Gene Expression Omnibus (GEO), accession GSE20966.
