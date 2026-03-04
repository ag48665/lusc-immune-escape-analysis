# Immune Landscape and Immune Escape in LUSC

Analysis of the immune microenvironment in **lung squamous cell carcinoma (LUSC)** using immune gene signatures and machine learning to characterize immune phenotypes and mechanisms of immune escape.

---

# Overview

Tumor immune microenvironments show substantial heterogeneity across patients. Understanding these differences is essential for predicting response to immunotherapy and identifying mechanisms of immune evasion.

In this project we analyze LUSC tumor samples using four immune gene signatures:

- Tumor Inflammation Signature (TIS)
- Cytotoxic T cell activity
- T cell exhaustion
- Tertiary lymphoid structures (TLS)

Dimensionality reduction and machine learning approaches reveal distinct immune phenotypes and regulatory mechanisms shaping tumor immune behavior.

---

# Key Findings

## Distinct immune phenotypes in LUSC tumors

UMAP-based immune landscape analysis revealed multiple tumor immune phenotypes:

- Inflamed
- Cold
- TLS-rich
- Exhausted

Inflamed tumors show strong immune activation and cytotoxic activity, while Cold tumors display minimal immune infiltration.

---

## Machine learning identifies immune activation as the primary driver

A **Random Forest classifier** was trained using immune signatures.

Results:

- Cross-validated accuracy ≈ **0.74**
- Most important feature: **Tumor Inflammation Signature (TIS)**
- Additional contributors: **TLS** and **cytotoxic activity**

These findings indicate that global immune activation represents the main axis structuring immune heterogeneity in LUSC tumors.

---

## Immune activation correlates with checkpoint signaling

Checkpoint score based on expression of key immune checkpoint genes:

PDCD1
CD274
CTLA4
LAG3
TIGIT
HAVCR2
ENTPD1
TOX


Immune activation strongly correlates with checkpoint signaling, suggesting a negative feedback regulatory mechanism that limits anti-tumor immune responses.

---

## Immune state model reveals functional and dysfunctional immune states

Tumors were categorized based on cytotoxicity and exhaustion:

| Immune State | Description |
|---|---|
| Cold | low cytotoxicity, low exhaustion |
| Functional | high cytotoxicity, low exhaustion |
| Suppressed | low cytotoxicity, high exhaustion |
| Exhausted | high cytotoxicity, high exhaustion |

Exhausted tumors exhibited significantly higher checkpoint signaling than other immune states.

---

## Immune trajectory toward exhaustion

An immune trajectory model suggests progression:

Cold → Functional cytotoxic → Exhausted → Immune escape


Chronic immune stimulation may drive progressive T cell exhaustion and checkpoint activation in inflamed tumors.

---

# Repository Structure

lusc-immune-escape-analysis
│
├── figures/ # Final figures
├── results_safe/ # Additional figures and results
├── LUSC_immune_escape_analysis.ipynb
├── genes.tsv
└── README.md


---

# Methods

Main computational approaches used:

- RNA-seq immune signature scoring
- UMAP dimensionality reduction
- Random Forest classification
- Feature importance analysis
- Correlation analysis
- Immune state modeling
- Pathway enrichment analysis

---

# Technologies

- Python
- Pandas
- NumPy
- Scikit-learn
- Seaborn
- Matplotlib
- UMAP
- Jupyter Notebook

---

# Biological Interpretation

The results support a model in which:

1. Immune activation promotes anti-tumor cytotoxic responses  
2. Chronic immune activation induces immune checkpoint pathways  
3. Persistent signaling leads to T cell exhaustion and immune escape

Understanding these processes may help identify tumors that respond to immune checkpoint blockade therapies.

---

# Author

Bioinformatics project exploring immune heterogeneity and immune escape mechanisms in lung cancer.
