# Transcriptomic Immune Profiling in Lung Squamous Cell Carcinoma (LUSC)

Transcriptomic immune profiling framework for characterizing immune activation, checkpoint signaling, and exhaustion-associated immune states in lung squamous cell carcinoma (LUSC) using TCGA and GEO datasets.

---

## Overview

This project investigates the immune landscape of lung squamous cell carcinoma (LUSC) using bulk transcriptomic datasets from:

- **TCGA-LUSC** (The Cancer Genome Atlas)
- **GEO GSE37745** validation cohort

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

## Key Findings

- Identification of heterogeneous immune states in LUSC tumors
- Strong correlation between immune activation and checkpoint signaling:
  - **TCGA-LUSC:** Pearson r = 0.88
  - **GEO GSE37745:** Pearson r = 0.84
- Distinct immune-cold and exhaustion-associated tumor phenotypes
- Reproducible immune organization visualized using UMAP
- No statistically significant overall survival differences between immune activation groups

---
## Potential Clinical Relevance

This project provides a transcriptomic framework for characterizing immune heterogeneity in lung squamous cell carcinoma (LUSC). By integrating immune activation, cytotoxicity, T-cell exhaustion, tertiary lymphoid structure, and checkpoint signaling signatures, the analysis identifies distinct immune states within LUSC tumors.

Although this work is exploratory and not intended for direct clinical decision-making, it may be useful for medical and translational research professionals in several ways:

- **Immune stratification of tumors:** The framework may help distinguish immune-cold tumors from inflamed tumors with cytotoxic and exhaustion-associated features.
- **Biomarker development:** The identified association between tumor inflammation and checkpoint signaling may support future development of transcriptomic biomarkers for immunotherapy response.
- **Immunotherapy research:** Tumors with high immune activation and high checkpoint signaling may represent biologically relevant candidates for further investigation in immune checkpoint inhibitor studies.
- **Clinical trial design:** Immune-state classification could potentially be used to define molecularly informed patient subgroups in retrospective or prospective translational studies.
- **Hypothesis generation:** The results may help generate hypotheses about adaptive immune resistance, T-cell exhaustion, and immune escape mechanisms in LUSC.

Importantly, survival analyses in this study did not show statistically significant differences between immune activation or exhaustion groups. Therefore, these findings should be interpreted as research-oriented and require further validation in immunotherapy-treated cohorts, single-cell datasets, spatial profiling studies, and protein-level assays before clinical application.

---


## Immune Signatures

### Tumor Inflammation Signature (TIS)

```text
CXCL9, CXCL10, CXCL11, IDO1, STAT1,
HLA-DRA, IFNG, CD8A, GZMB, PRF1
```

### Cytotoxicity Signature

```text
CD8A, CD8B, NKG7, PRF1, GNLY, GZMB
```

### Exhaustion Signature

```text
PDCD1, CTLA4, LAG3, TIGIT,
HAVCR2, TOX, ENTPD1
```

### TLS Signature

```text
CCL19, CCL21, CXCL13, CCR7,
CXCR5, CD79A, MS4A1
```

### Checkpoint Signaling Signature

```text
PDCD1, CD274, CTLA4, TIGIT,
LAG3, HAVCR2, IDO1, ENTPD1
```

---

## Immune State Classification

Tumors were stratified into four transcriptomic immune states:

1. Cytotoxic-high / exhaustion-high
2. Cytotoxic-high / exhaustion-low
3. Cytotoxic-low / exhaustion-high
4. Immune-cold tumors

Classification was based on median-based signature thresholds across the TCGA-LUSC cohort.

---

## Methods Summary

### Data Sources

- TCGA-LUSC transcriptomic and clinical data
- GEO dataset GSE37745 for external validation

### Analytical Workflow

- Gene expression normalization using z-score scaling
- Signature score calculation
- UMAP dimensionality reduction
- Correlation analysis
- Kaplan–Meier survival analysis

### Technologies

- Python 3.12
- pandas
- NumPy
- SciPy
- seaborn
- matplotlib
- lifelines
- umap-learn

---

## Repository Structure

```text
lusc-immune-escape-analysis/
│
├── data/
│   ├── tcga/
│   └── geo/
│
├── notebooks/
│   ├── preprocessing.ipynb
│   ├── immune_signatures.ipynb
│   ├── umap_analysis.ipynb
│   └── survival_analysis.ipynb
│
├── scripts/
│   ├── preprocessing.py
│   ├── signatures.py
│   ├── visualization.py
│   └── survival.py
│
├── figures/
│
├── results/
│
├── requirements.txt
└── README.md
```

---

## Installation

Clone the repository:

```bash
git clone https://github.com/ag48665/lusc-immune-escape-analysis.git
cd lusc-immune-escape-analysis
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

## Example Workflow

### 1. Preprocess transcriptomic data

```bash
python scripts/preprocessing.py
```

### 2. Calculate immune signatures

```bash
python scripts/signatures.py
```

### 3. Generate immune landscape visualization

```bash
python scripts/visualization.py
```

### 4. Run survival analysis

```bash
python scripts/survival.py
```

---

## Results

The analysis demonstrates that highly inflamed tumors exhibit coordinated activation of inhibitory immune regulatory programs associated with T-cell exhaustion and adaptive immune resistance.

These findings support the use of transcriptomic immune profiling for:

- Immune stratification in LUSC
- Characterization of checkpoint-associated immune states
- Biomarker discovery for immunotherapy research

---

## Validation

Key findings were independently validated in the GEO GSE37745 cohort, confirming the reproducibility of the immune activation–checkpoint signaling relationship across datasets.

---

## Citation

If you use this repository or analysis framework, please cite:

> Gabara A. *Transcriptomic immune profiling identifies checkpoint-associated immune states in lung squamous cell carcinoma.*

---

## Data Availability

Datasets used in this study are publicly available:

- TCGA-LUSC
- GEO: GSE37745

Repository:
https://github.com/ag48665/lusc-immune-escape-analysis

---

## License

MIT License

---

## Author

**Agata Gabara**  
Independent Researcher  
Koluszki, Poland

Email: agatagabara@gmail.com
