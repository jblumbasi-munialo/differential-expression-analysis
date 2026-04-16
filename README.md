[README (2).md](https://github.com/user-attachments/files/26783389/README.2.md)
# 🧬 Differential Expression Analysis with Blockchain & Machine Learning

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://python.org)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Bioinformatics](https://img.shields.io/badge/Bioinformatics-Cancer-red.svg)](https://github.com)

## 📊 Project Overview

A comprehensive **differential expression analysis** pipeline comparing **tumor vs normal** tissue samples using TCGA breast cancer data, enhanced with:

- 🔗 **Blockchain Technology** - Immutable records with SHA-256 hashing
- 🤖 **Machine Learning** - Random Forest classification of regulation direction
- 📈 **Interactive Visualizations** - Publication-ready figures
- 🔬 **Clinical Interpretation** - Actionable insights for precision medicine

---

## 🎯 Key Findings

### Differential Expression Summary

| Metric | Value |
|--------|-------|
| **Total Genes Analyzed** | 97 |
| **Significant DEGs** (FDR < 0.01) | 97 |
| **Up-regulated Genes** | 86 |
| **Down-regulated Genes** | 11 |

### 🔴 Top Up-regulated Genes (Oncogenes)

| Rank | Gene | Log2 Fold Change | P-adjusted | Clinical Relevance |
|------|------|-----------------|------------|---------------------|
| 1 | **ERBB2** | 3.98 | 6.15e-30 | Herceptin target |
| 2 | **CST1** | 3.53 | 1.27e-29 | Invasion marker |
| 3 | **COL10A1** | 3.36 | 3.13e-21 | Tumor stroma |
| 4 | **MKI67** | 3.34 | 8.28e-26 | Proliferation marker |
| 5 | **MMP13** | 3.32 | 2.46e-24 | Metastasis |
| 6 | **MYC** | 3.14 | 2.26e-23 | Master oncogene |
| 7 | **CCND1** | 2.97 | 1.71e-20 | Cell cycle |
| 8 | **MMP1** | 2.63 | 1.27e-21 | Invasion |
| 9 | **KRAS** | 2.50 | 4.75e-18 | Oncogene |
| 10 | **TOP2A** | 2.47 | 4.93e-24 | Chemo target |

### 🔵 Top Down-regulated Genes (Tumor Suppressors)

| Rank | Gene | Log2 Fold Change | P-adjusted | Clinical Relevance |
|------|------|-----------------|------------|---------------------|
| 1 | **LEP** | -2.73 | 1.08e-21 | Adipokine |
| 2 | **ESR1** | -2.70 | 1.08e-21 | Endocrine therapy marker |
| 3 | **CA4** | -2.70 | 1.82e-19 | Carbonic anhydrase |
| 4 | **ADIPOQ** | -2.17 | 4.85e-16 | Adiponectin |
| 5 | **SCARA5** | -1.98 | 3.67e-15 | Scavenger receptor |
| 6 | **PGR** | -1.79 | 8.05e-09 | Progesterone receptor |
| 7 | **FOXA1** | -1.65 | 3.34e-11 | Pioneer factor |
| 8 | **GATA3** | -1.54 | 1.55e-06 | Transcription factor |
| 9 | **PTEN** | -1.26 | 2.89e-06 | Tumor suppressor |
| 10 | **CDH1** | -1.14 | 6.03e-05 | E-cadherin |

---

## 🔗 Blockchain Integration

### Features

| Feature | Description |
|---------|-------------|
| **Immutable Records** | SHA-256 cryptographic hashing |
| **Audit Trail** | Complete history of top DEGs |
| **Proof-of-Work** | Mining difficulty level 3 |
| **Chain Validation** | Automatic integrity checking |
| **Timestamping** | Permanent time records |

### Blockchain Statistics

```
┌─────────────────────────────────────────┐
│  Blockchain Status                      │
├─────────────────────────────────────────┤
│  Blocks: 16                             │
│  Chain Valid: True                      │
│  Difficulty: 3                          │
│  Top DEGs Recorded: 15                  │
└─────────────────────────────────────────┘
```

---

## 🤖 Machine Learning

### Model Performance

| Model | Task | Accuracy | Cross-Validation |
|-------|------|----------|------------------|
| **Random Forest** | Up vs Down Classification | 95%+ | 5-fold CV |

### Feature Importance

```
Feature Importance for Regulation Classification:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
  log2FoldChange  ████████████████████████████████████  0.95
  pvalue          ██                                     0.05
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### Prediction Capabilities

- ✅ Predicts regulation direction (up/down) for new genes
- ✅ Identifies borderline genes likely to become significant
- ✅ Confidence scores for each prediction

---

## 📁 Repository Structure

```
differential-expression-analysis/
│
├── 📊 data/                          # Expression data and DEG results
│   ├── differential_expression_results.csv
│   ├── upregulated_genes.csv
│   └── downregulated_genes.csv
│
├── 📈 figures/                       # Visualizations
│   ├── volcano_plot.png              # -log10(p) vs log2FC
│   ├── deg_heatmap.png               # Expression heatmap
│   ├── pca_plot.png                  # Sample clustering
│   └── blockchain_ml_analysis.png    # Blockchain + ML summary
│
├── 🔗 blockchain/                    # Immutable records
│   └── deg_blockchain_ledger.csv     # SHA-256 hashed blocks
│
├── 🤖 results/                       # Machine learning outputs
│   ├── regulation_predictions.csv    # Up/down predictions
│   └── ml_feature_importance.csv     # Feature importance scores
│
├── 📄 README.md                      # This file
├── 📄 requirements.txt               # Python dependencies
└── 📄 analyze_results.py             # Reproducible analysis script
```

---

## 🚀 Quick Start

### Installation

```bash
# Clone the repository
git clone https://github.com/jblumbasi-munialo/differential-expression-analysis.git
cd differential-expression-analysis

# Install dependencies
pip install -r requirements.txt
```

### Run Analysis

```python
import pandas as pd
import matplotlib.pyplot as plt

# Load differential expression results
results = pd.read_csv('data/differential_expression_results.csv')
print(f'Total genes analyzed: {len(results)}')

# View top up-regulated genes
up_genes = results[results['log2FoldChange'] > 1].nlargest(10, 'log2FoldChange')
print(up_genes[['gene', 'log2FoldChange', 'padj']])

# Load blockchain ledger
ledger = pd.read_csv('blockchain/deg_blockchain_ledger.csv')
print(f'Blockchain records: {len(ledger)} blocks')

# Load ML predictions
predictions = pd.read_csv('results/regulation_predictions.csv')
print(predictions.head())
```

---

## 🔬 Methods

### Data Source
- **TCGA Breast Cancer (BRCA)**
- **Samples**: 200 (tumor vs normal)
- **Analysis**: Differential expression (t-test + FDR correction)

### Statistical Analysis

| Parameter | Value |
|-----------|-------|
| Significance Threshold | FDR < 0.01 |
| Fold Change Threshold | |log2FC| > 1 |
| Multiple Testing | Benjamini-Hochberg |

### Blockchain Implementation

```python
# Each block contains:
# - Gene name
# - Log2 fold change
# - Adjusted p-value
# - SHA-256 hash of previous block
# - Proof-of-work nonce
```

### Machine Learning

| Parameter | Value |
|-----------|-------|
| Algorithm | Random Forest |
| Trees | 100 |
| Test Size | 30% |
| Cross-validation | 5-fold |

---

## 💊 Clinical Implications

| Gene | Clinical Application | Evidence |
|------|---------------------|----------|
| **ERBB2 (HER2)** | Trastuzumab (Herceptin) | FDA Approved |
| **ESR1** | Tamoxifen/Endocrine therapy | Standard of care |
| **MKI67 (Ki-67)** | Proliferation index | Prognostic marker |
| **TOP2A** | Anthracycline sensitivity | Predictive marker |
| **PTEN** | PI3K inhibitor sensitivity | Emerging target |

---

## 📊 Results Visualization

### Volcano Plot
![Volcano Plot](figures/volcano_plot.png)

### Expression Heatmap
![Heatmap](figures/deg_heatmap.png)

### Blockchain + ML Analysis
![Blockchain ML](figures/blockchain_ml_analysis.png)

---

## 📝 Citation

```bibtex
@misc{DifferentialExpressionBlockchainML2026,
  author = {HCMI-CMDC Research Team},
  title = {Differential Expression Analysis with Blockchain and Machine Learning},
  year = {2026},
  publisher = {GitHub},
  url = {https://github.com/jblumbasi-munialo/differential-expression-analysis}
}
```

---

## 📧 Contact

For questions or collaboration inquiries, please open an issue on GitHub.

---

**⭐ Star this repository if you found it useful!**

---
*Generated by HCMI-CMDC Bioinformatics Pipeline*
