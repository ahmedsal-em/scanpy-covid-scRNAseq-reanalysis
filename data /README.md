# 📊 Dataset Instructions

The dataset used in this project is publicly available from the Gene Expression Omnibus (GEO).

## 📦 Dataset

- **Accession:** GSE272840  
- **Title:** SARS-CoV-2 viscRNA-seq in alveolar organoids  

## 🔗 Download Link

https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE272840

## 📁 Required File

Download the processed AnnData file and place it in this directory:
data/GSE272840_ALO_viscRNAseq.h5ad

## ⚠️ Notes

- The dataset is not included in this repository due to its size.
- Make sure the filename matches exactly, otherwise the notebook will not run.
- No preprocessing is required — the file is already formatted for Scanpy.

---

## 🚀 Usage

After placing the file in the `data/` folder, you can run:
notebooks/data_full_analysis.ipynb
