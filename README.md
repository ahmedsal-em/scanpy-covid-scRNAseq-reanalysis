# 🧬 Scanpy Re-analysis of SARS-CoV-2 viscRNA-seq Dataset (GSE272840)

![Status](https://img.shields.io/badge/status-complete-success)
![Python](https://img.shields.io/badge/python-3.x-blue)
![Scanpy](https://img.shields.io/badge/scanpy-scRNA--seq-orange)

An independent **single-cell RNA-seq re-analysis** of **GSE272840** using **Python** and **Scanpy** to investigate:

- 🦠 SARS-CoV-2 infection response
- 🧫 epithelial cell-state structure
- 💊 transcriptional effects of **RMC-113**

---

## 📌 Overview

This project reproduces and extends the analysis of a public **viscRNA-seq** dataset from alveolar organoids.  
The workflow includes:

- quality control and filtering
- normalization and highly variable gene selection
- PCA, UMAP, and Leiden clustering
- marker-based cell-type interpretation
- infection-response analysis
- treatment-effect analysis

---

## 📊 Dataset

**GEO Accession:** GSE272840  

Download from GEO:  
https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE272840  

Place the file in:
data/GSE272840_ALO_viscRNAseq.h5ad

---

## 📁 Project Structure
scanpy-covid-scRNAseq-reanalysis/
├── notebooks/
│   └── data_full_analysis.ipynb
│
├── data/
│   └── GSE272840_ALO_viscRNAseq.h5ad
│
├── figures/
│   ├── Figure_04_pca_variance.png
│   ├── Figure_07_umap_celltypes.png
│   ├── Figure_11_section_06_celltype_response_24h.png
│   ├── Figure_12_section_07_celltype_abundance.png
│   └── Figure_13_section_08_drug_effect_24h.png
│
├── README.md
└── requirements.txt

---

## 🧪 Analysis Workflow

- 🔍 Data loading and inspection  
- 🧫 Experimental condition analysis  
- 📊 Quality control and filtering  
- ⚙️ Normalization and log transformation  
- 🔬 Highly variable gene selection  
- 📏 Scaling and PCA  
- 🧭 Clustering (Leiden) and UMAP  
- 🧬 Marker gene analysis  
- 🏷 Cell-type annotation  
- 🦠 Infection response analysis  
- 💊 Drug effect analysis  

---

## 🔬 Key Results

### 🧭 Cell-type identification

UMAP reveals clear separation of epithelial populations:

- AT2-like cells  
- AT1-like cells  
- Basal-like cells  
- NGFR-HOPX-CEACAM6+ cells  

---

### 🧬 Infection response (24h)

- Strong **cell-type-specific transcriptional changes**  
- Distinct responses between AT1-like and AT2-like cells  

---

### 📊 Cell-type abundance changes

- Increase in basal-like cells  
- Decrease in AT2-like cells  
- Evidence of epithelial remodeling  

---

### 💊 Drug effect (RMC-113)

- Drug alters infection-related gene expression  
- Partial normalization of transcriptional response  

---

## 🧰 Requirements

Install dependencies:
pip install -r requirements.txt

---

## 🚀 Key Takeaways

- ✅ Clear identification of epithelial cell types  
- 🦠 Strong infection response  
- 🔄 Dynamic population changes  
- 💊 Drug-modulated transcriptional effects  

---

## 👨‍💻 Author

Ahmed Salem  

Independent computational re-analysis using Python and Scanpy  

---

## 📄 Related Publication

**Karim et al., Nature Communications (2025)**  

🔗 [Single-cell viscRNA-seq analysis of SARS-CoV-2 infection in alveolar organoids](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE272840)

---

## ⭐ If you find this useful

Give the repo a ⭐
