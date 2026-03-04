# Immune Landscape and Immune Escape in LUSC

[![Python](https://img.shields.io/badge/Python-3.9-blue)]()
[![License](https://img.shields.io/badge/License-MIT-green)]()
[![Status](https://img.shields.io/badge/status-research-orange)]()

Computational analysis of the **immune microenvironment in lung squamous cell carcinoma (LUSC)** using immune gene signatures, dimensionality reduction, and machine learning.

This repository explores how **immune activation, cytotoxicity, tertiary lymphoid structures (TLS), and T-cell exhaustion** shape tumor immune phenotypes and drive mechanisms of **immune escape**.

---

# Graphical Abstract

![Graphical Abstract](results_safe/FIG_GRAPHICAL_ABSTRACT_immune_escape.png)

Conceptual model of immune landscape organization and progression toward immune exhaustion in LUSC tumors.

---

# Study Overview

Tumor immune microenvironments show substantial heterogeneity across patients. Understanding these differences is critical for predicting response to immunotherapy and identifying mechanisms of tumor immune evasion.

This study quantifies four immune gene signatures:

- **Tumor Inflammation Signature (TIS)**
- **Cytotoxic T-cell activity**
- **T-cell exhaustion**
- **Tertiary lymphoid structures (TLS)**

These immune programs capture major axes of tumor immune behavior.

---

# Key Findings

## Immune landscape reveals distinct tumor phenotypes

UMAP projection of immune signatures revealed heterogeneous tumor immune landscapes with four major phenotypes:

- Inflamed
- Cold
- TLS-rich
- Exhausted

Inflamed tumors display strong immune activation and cytotoxic signaling, while Cold tumors show minimal immune infiltration.

---

## Machine learning identifies immune activation as the dominant driver

A **Random Forest classifier** was trained using immune signatures.

Results:

- Cross-validated accuracy ≈ **0.74**
- Most informative feature: **Tumor Inflammation Signature (TIS)**
- Additional contributors: **TLS** and **cytotoxic activity**

These findings indicate that **global immune activation is the primary axis structuring immune heterogeneity in LUSC tumors**.

---

## Immune activation correlates with checkpoint signaling

Checkpoint signaling score was computed using the expression of key immune checkpoint genes:

PDCD1
CD274
CTLA4
LAG3
TIGIT
HAVCR2
ENTPD1
TOX


Immune activation strongly correlates with checkpoint signaling, suggesting a **negative feedback mechanism that limits anti-tumor immunity**.

---

## Immune state model

Tumors were classified into immune states based on cytotoxicity and exhaustion.

| Immune State | Cytotoxicity | Exhaustion |
|---|---|---|
| Cold | Low | Low |
| Functional | High | Low |
| Suppressed | Low | High |
| Exhausted | High | High |

Exhausted tumors show significantly higher checkpoint signaling.

---

## Immune trajectory model

The data suggest a potential progression:

Cold → Functional cytotoxic → Exhausted → Immune escape


Chronic immune stimulation may drive progressive **T-cell exhaustion and checkpoint activation**.

---

# Example Figures

## Immune landscape

![UMAP landscape](results_safe/FIG_UMAP_panel_subtype_TIS_TLS_EXH_CYTO.png)

UMAP projection of immune signatures revealing heterogeneous tumor immune phenotypes.

---

## Immune activation vs checkpoint signaling

Immune activation strongly correlates with checkpoint expression across tumors.

---

## Immune state diagram

![Immune states](results_safe/FIG_immune_state_diagram.png)

Functional and dysfunctional immune states defined by cytotoxicity and exhaustion.

---

# Repository Structure
lusc-immune-escape-analysis
│
├── figures/ # Final manuscript figures
├── results_safe/ # Additional plots and exploratory analyses
├── LUSC_immune_escape_analysis.ipynb
├── genes.tsv
└── README.md


---

# Methods

Computational approaches used:

- RNA-seq immune signature scoring
- UMAP dimensionality reduction
- Random Forest classification
- Feature importance analysis
- Correlation analysis
- Immune state modeling
- Pathway enrichment analysis
- Gene network analysis

---

# Technologies

Python ecosystem:

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- UMAP
- Jupyter Notebook

---

# Biological Interpretation

The results support a model in which:

1. Tumor immune activation promotes cytotoxic anti-tumor responses  
2. Chronic immune stimulation induces checkpoint signaling  
3. Persistent checkpoint activation drives **T-cell exhaustion**  
4. This leads to **immune escape**

Understanding these transitions may help identify tumors responsive to **immune checkpoint blockade therapies**.

---
# Figure Gallery

## Immune Landscape

![UMAP immune landscape](results_safe/FIG_UMAP_panel_subtype_TIS_TLS_EXH_CYTO.png)

![UMAP immune subtypes](results_safe/UMAP_immune_subtypes.png)

![PCA immune subtypes](results_safe/PCA_immune_subtypes.png)

---

## Immune Activation and Checkpoint Signaling

![Activation vs checkpoints](results_safe/FIG_activation_to_checkpoints.png)

![Activation vs checkpoints by subtype](results_safe/FIG3B_activation_to_checkpoints_by_subtype.png)

![Checkpoint signaling across states](results_safe/FIG4_checkpoint_across_states.png)

![Checkpoint medians](results_safe/FIG4_checkpoint_medians.png)

![Checkpoint network](results_safe/FIG_checkpoint_network.png)

---

## Immune State Models

![Immune state diagram](results_safe/FIG_immune_state_diagram.png)

![Cytotoxic vs exhaustion](results_safe/FIG_cytotoxic_vs_exhaustion_state.png)

![Immune trajectory](results_safe/FIG5_immune_trajectory.png)

---

## Machine Learning Analysis

![Feature importance](results_safe/FIG_ML_feature_importance.png)

![Confusion matrix](results_safe/FIG_ML_confusion_matrix.png)

![ROC multiclass](results_safe/FIG_ML_CV_ROC_multiclass.png)

![SHAP summary](results_safe/FIG_SHAP_summary.png)

![SHAP feature importance](results_safe/FIG_SHAP_bar_importance.png)

---

## Immune Signatures

![Immune signatures heatmap](results_safe/immune_signatures_heatmap_log2FC.png)

![Immune signatures summary](results_safe/immune_signatures_summary_bar.png)

![Clustermap signatures](results_safe/FIG_clustermap_samples_signatures.png)

![Dendrogram signatures](results_safe/FIG_dendrogram_samples_signatures.png)

---

## Pathway and Gene Network Analysis

![Pathway enrichment](results_safe/FIG_pathway_enrichment.png)

![Gene network](results_safe/FIG_gene_network_thr0.55.png)

---

## Differential Expression

![Volcano plot hot vs cold](results_safe/volcano_hot_vs_cold.png)

![Volcano Welch test](results_safe/volcano_Welch_hot_vs_cold.png)

![Top genes volcano](results_safe/volcano_labeled_TOP10.png)

---

## Immune Cell Infiltration

![Immune cell infiltration](results_safe/immune_cell_infiltration.png)

![Immune infiltration visualization](results_safe/immune_cell_infiltration_pretty.png)

---

## Heatmaps

![Top genes heatmap](results_safe/heatmap_top30.png)

![TLS immune heatmap](results_safe/heatmap_TLS_T_NK_IFNg_log2FC.png)

---

# Citation

If you use this repository or analysis framework, please cite:

Immune Landscape and Immune Escape in LUSC
Computational analysis of tumor immune phenotypes using immune gene signatures and machine learning.


---

# Author

Bioinformatics project exploring **immune heterogeneity and immune escape mechanisms in lung cancer**.
