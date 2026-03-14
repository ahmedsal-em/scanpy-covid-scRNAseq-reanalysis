# scanpy-covid-scRNAseq-reanalysis
Independent re-analysis of Karim et. al. published single-cell RNA-seq dataset using Python

## Step 1: Load the data

The processed single-cell dataset is available from GEO under accession **GSE272840**.

Download:
- `GSE272840_ALO_viscRNAseq.h5ad`
- https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE272840

Move the file to:
- `data/GSE272840_ALO_viscRNAseq.h5ad`

The dataset will then be loaded in Python using Scanpy for inspection of:
- number of cells and genes
- sample metadata
- experimental conditions
- available annotations
