# 🧬 Scanpy Re-analysis of SARS-CoV-2 viscRNA-seq Dataset (GSE272840)

![Status](https://img.shields.io/badge/Status-Completed-success)

![Tool](https://img.shields.io/badge/Tool-Scanpy-blue)

![Language](https://img.shields.io/badge/Language-Python-yellow)

This repository presents an **independent re-analysis of single-cell RNA-seq data** from:

**Karim et al., Nature Communications (2025)**  

We use **Scanpy (Python)** to study:

- 🦠 SARS-CoV-2 infection  

- 💊 RMC-113 drug treatment  

- 🧫 Epithelial cell-type responses  

---

## 📁 Project Structure

scanpy-covid-scRNAseq-reanalysis/
├── notebooks/
├── data/
├── figures/
├── README.md
└── requirements.txt

---

## 📊 Dataset

**GEO Accession:** GSE272840  

Download from GEO:  
https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE272840  

Place the file in:
data/GSE272840_ALO_viscRNAseq.h5ad

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

## ⭐ If you find this useful

Give the repo a ⭐
