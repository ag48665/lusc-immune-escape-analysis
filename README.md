# Transcriptomic Immune Profiling in Lung Squamous Cell Carcinoma (LUSC)

Transcriptomic immune profiling framework for characterizing immune activation, checkpoint signaling, and exhaustion-associated immune states in lung squamous cell carcinoma (LUSC) using TCGA and GEO datasets.

---

## Project Overview

This project investigates the immune landscape of lung squamous cell carcinoma (LUSC) using bulk transcriptomic datasets from:

- **TCGA-LUSC (The Cancer Genome Atlas)**
- **GEO GSE37745 external validation cohort**

The analysis focuses on:

- Tumor inflammation signatures (TIS)
- Cytotoxic T-cell activity
- T-cell exhaustion programs
- Immune checkpoint signaling
- Tertiary lymphoid structure (TLS) signatures
- Immune landscape visualization using UMAP
- Survival analysis of immune states

The study identifies reproducible associations between immune activation and checkpoint signaling across independent cohorts.

---

## Project Highlights

✔ TCGA-LUSC transcriptomic analysis

✔ External validation using GEO GSE37745

✔ Tumor inflammation signature (TIS)

✔ T-cell exhaustion profiling

✔ Immune checkpoint signaling analysis

✔ UMAP immune landscape visualization

✔ Kaplan–Meier survival analysis

✔ Reproducible Python workflow

---

## Key Findings

- Identification of heterogeneous immune states in LUSC tumors

- Strong correlation between immune activation and checkpoint signaling:

  - **TCGA-LUSC:** Pearson r = 0.88
  - **GEO GSE37745:** Pearson r = 0.84

- Distinct immune-cold and exhaustion-associated tumor phenotypes

- Reproducible immune organization visualized using UMAP

- No statistically significant overall survival differences between immune activation groups

---

## Main Figures

### Figure 1. Transcriptomic Immune Landscape of TCGA-LUSC Tumors

<img src="figures/Figure 1. Transcriptomic immune landscape of TCGA-LUSC tumors.png" width="900">

UMAP visualization reveals heterogeneous immune organization and distinct transcriptomic immune states across LUSC tumors.

---

### Figure 2. Association Between Immune Activation and Checkpoint Signaling

<img src="figures/Figure 2. Association between immune activation and checkpoint signaling.png" width="900">

Strong positive association between tumor inflammation signatures and immune checkpoint activity.

---

### Figure 3. External Validation of Immune Activation and Checkpoint Signaling

<img src="figures/Figure 3. Independent validation of immune activation and checkpoint signaling.png" width="900">

Independent GEO cohort confirms the immune activation–checkpoint signaling relationship.

---

### Figure 4. Kaplan–Meier Survival Analysis

<img src="figures/Figure 4. Kaplan–Meier survival analysis according to exhaustion-associated immune states.png" width="900">

Overall survival comparison between transcriptomic immune states.

---

### Table 1. Clinical and Transcriptomic Characteristics

<img src="figures/Table 1. Clinical and transcriptomic characteristics of the TCGA-LUSC cohort.png" width="900">

Summary of clinical and transcriptomic characteristics used throughout the study.

---

## Potential Clinical Relevance

This project provides a transcriptomic framework for characterizing immune heterogeneity in lung squamous cell carcinoma (LUSC).

Potential applications include:

- Immune stratification of tumors
- Identification of immune-cold versus inflamed tumors
- Biomarker discovery for immunotherapy research
- Investigation of adaptive immune resistance mechanisms
- Translational cancer immunology studies
- Hypothesis generation for future checkpoint inhibitor research

Importantly, this project is intended for research and educational purposes and is not designed for clinical decision-making.

---

## Immune Signatures

### Tumor Inflammation Signature (TIS)

```text
CXCL9
CXCL10
CXCL11
IDO1
STAT1
HLA-DRA
IFNG
CD8A
GZMB
PRF1
