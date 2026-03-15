# Scanpy Re-analysis of SARS-CoV-2 viscRNA-seq Dataset (GSE272840)

This repository contains an **independent re-analysis of the single-cell RNA-seq dataset GSE272840** published by:

**Karim et al., Nature Communications (2025)**

The analysis is performed using **Python and Scanpy** to reproduce and explore transcriptional responses to **SARS-CoV-2 infection** and **RMC-113 drug treatment**.

---

# Project Structure

scanpy-covid-scRNAseq-reanalysis/
│
├── notebooks/
│   └── data_full_analysis.ipynb
│
├── data/
│   └── GSE272840_ALO_viscRNAseq.h5ad
│
├── figures/
│
├── README.md
└── requirements.txt

---

# Dataset

The processed single-cell dataset is available from **GEO**.

**Accession:** GSE272840

Download from GEO:

https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE272840

Place the downloaded file in: data/GSE272840_ALO_viscRNAseq.h5ad

---

# Analysis Workflow

The notebook performs a full single-cell RNA-seq analysis pipeline using **Scanpy**.

---

# 1. Load and Inspect Dataset

The AnnData object is loaded and inspected to explore the dataset structure.

This includes:

- cell metadata (`obs`)
- gene metadata (`var`)
- dataset dimensions
- experimental annotations

---

# 2. Inspect Experimental Conditions

The dataset contains **eight experimental conditions** combining:

- timepoint (4h / 24h)
- infection status
- drug treatment

Cell counts per condition are inspected to verify dataset balance.

---

# 3. Cell Distribution Across Conditions

A bar plot visualizes the number of cells captured for each experimental condition.

This ensures representation across:

- infected samples
- uninfected controls
- drug-treated samples
- control treatments

---

# 4. Quality Control Assessment

Standard single-cell QC metrics are evaluated:

- number of detected genes per cell
- total counts per cell
- mitochondrial RNA percentage

Visualizations include:

- violin plots
- scatter plots
- histograms

These plots help identify low-quality cells.

---

# 5. Filter Low-Quality Cells

Cells are filtered based on QC thresholds:

- **> 500 genes detected**
- **< 8000 genes detected**
- **< 20% mitochondrial RNA**

This step removes:

- low-quality cells
- dying cells
- potential doublets.

---

# 6. Normalize and Log Transform

Gene expression counts are normalized per cell to correct for sequencing depth.

Processing steps:

1. normalize counts to **10,000 counts per cell**
2. apply **log transformation**

---

# 7. Select Highly Variable Genes

Highly variable genes (HVGs) capture the most informative transcriptional variation.

The **top 2000 HVGs** are selected using the Seurat method.

Only these genes are retained for downstream analyses.

---

# 8. Scale Data

Gene expression values are scaled to:

- zero mean
- unit variance

This prepares the data for PCA.

---

# 9. Principal Component Analysis (PCA)

PCA reduces dimensionality and identifies the main axes of transcriptional variation.

Outputs include:

- PCA variance ratio plot
- PCA scatter plots.

---

# 10. Neighbor Graph, UMAP, and Clustering

A neighborhood graph is constructed in PCA space.

Then:

- UMAP is computed for visualization
- Leiden clustering identifies transcriptionally distinct cell populations.

---

# 11. Marker Gene Analysis

Differential expression analysis identifies marker genes for each Leiden cluster.

Visualizations include:

- ranked gene plots
- cluster dotplots
- heatmaps of marker expression.

---

# 12. Cell Type Annotation

Leiden clusters are compared with **author-provided cell-type labels**.

The four epithelial populations are:

- AT2-like cells
- AT1-like cells
- NGFR-HOPX-CEACAM6+
- Basal-like cells

UMAP visualizations confirm the spatial distribution of these cell types.

---

# 13. Global Infection Response (DMSO Control)

To isolate the effect of infection, infected and uninfected cells are compared under **DMSO control**.

Two analyses are performed:

- **4h infection response**
- **24h infection response**

Differential expression results are visualized with dotplots.

---

# 14. QC Check on Uninfected Cells Across Time

Uninfected cells at **4h vs 24h** are compared to confirm that transcriptional differences are not driven solely by time.

UMAP visualizations confirm consistent cell-type distributions across timepoints.

---

# 15. Global Infection Response Under RMC-113 Treatment

Infection response is also analyzed in the presence of **RMC-113 treatment**.

Comparisons are performed at:

- 4h
- 24h

This allows investigation of infection-induced transcriptional programs under drug treatment.

---

# 16. Drug Effect During Infection

The transcriptional impact of **RMC-113** is assessed by comparing:
infected RMC-113 vs infected DMSO

Analyses are performed for:

- **4h infection**
- **24h infection**

This identifies drug-responsive transcriptional changes.

---

# 17. Cell-Type Specific Infection Response (4h)

Infection responses are analyzed within specific epithelial populations.

Example analysis:
- Basal-like cells
- infected vs uninfected

This identifies cell-type-specific transcriptional programs during early infection.

---

# 18. Cell-Type Specific Infection Response (24h)

The same analysis is performed at **24 hours** for each epithelial population:

- AT2-like cells
- AT1-like cells
- Basal-like cells
- NGFR-HOPX-CEACAM6+

Differential expression results are visualized using dotplots.

---

# 19. Infection Response Summary Across Cell Types

Top infection-responsive genes from each epithelial population are combined into summary visualizations:

- heatmaps
- dotplots

This highlights shared and cell-type-specific transcriptional responses.

---

# 20. Cell-Type Abundance Changes

The proportion of epithelial populations is compared between infected vs uninfected

Stacked bar plots reveal shifts in epithelial composition during infection.

---

# 21. Drug Effect on Infection Pathways

Finally, transcriptional differences between **RMC-113 and DMSO treatment** during infection are examined.

Differential expression identifies genes associated with drug-modulated infection pathways.

---

# Requirements

Install required packages:
- pip install -r requirements.txt

---

# Author

Ahmed Salem

Independent computational re-analysis project using Python and Scanpy.

---

# Related Publication

Karim et al., Nature Communications (2025)

Single-cell viscRNA-seq analysis of SARS-CoV-2 infection in alveolar organoids.
