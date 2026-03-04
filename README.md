# Immune Landscape and Immune Escape in LUSC

Computational analysis of the immune microenvironment in **lung squamous cell carcinoma (LUSC)** using immune gene signatures, dimensionality reduction, and machine learning.

This project investigates how **immune activation, cytotoxicity, tertiary lymphoid structures (TLS), and T cell exhaustion** shape tumor immune phenotypes and contribute to immune escape.

---

## Graphical Summary

The analysis suggests a potential immune trajectory:

Cold tumors → immune activation → cytotoxic response → T cell exhaustion → immune escape

Chronic immune stimulation may induce checkpoint signaling that limits anti-tumor immunity.

---

## Key Immune Signatures

Four immune programs were quantified across tumor samples:

- **Tumor Inflammation Signature (TIS)**
- **Cytotoxic T cell activity**
- **T cell exhaustion**
- **Tertiary lymphoid structures (TLS)**

These signatures capture major dimensions of tumor immune behavior.

---

## Main Findings

### Distinct immune phenotypes in LUSC

UMAP projection of immune signatures revealed heterogeneous tumor immune landscapes with four dominant phenotypes:

- **Inflamed**
- **Cold**
- **TLS-rich**
- **Exhausted**

Inflamed tumors display strong immune activation and cytotoxic signaling, while Cold tumors show minimal immune infiltration.

---

### Machine learning identifies immune activation as the dominant driver

A **Random Forest classifier** was trained using immune signatures.

Key results:

- Cross-validated accuracy ≈ **0.74**
- Most informative feature: **Tumor Inflammation Signature (TIS)**
- Additional contributors: **TLS** and **cytotoxic activity**

These findings indicate that **global immune activation is the primary axis structuring immune heterogeneity in LUSC tumors**.

---

### Immune activation correlates with checkpoint signaling

Checkpoint signaling score based on expression of key immune checkpoint genes:

PDCD1
CD274
CTLA4
LAG3
TIGIT
HAVCR2
ENTPD1
TOX


Immune activation strongly correlates with checkpoint signaling, suggesting a **negative feedback regulatory mechanism** that suppresses T-cell activity.

---

### Immune state model

Tumors were classified into four immune states based on cytotoxicity and exhaustion:

| Immune State | Cytotoxicity | Exhaustion |
|---|---|---|
| Cold | Low | Low |
| Functional | High | Low |
| Suppressed | Low | High |
| Exhausted | High | High |

Exhausted tumors exhibited **significantly higher checkpoint signaling** than other states.

---

### Immune trajectory toward exhaustion

The data suggest a progression model:

Cold → Functional cytotoxic → Exhausted → Immune escape


Persistent immune activation may drive checkpoint upregulation and **progressive T-cell dysfunction**.

---

## Repository Structure

lusc-immune-escape-analysis
│
├── figures/ # Final manuscript figures
├── results_safe/ # Additional results and exploratory plots
├── LUSC_immune_escape_analysis.ipynb
├── genes.tsv
└── README.md


---

## Methods

Computational approaches used in this project:

- RNA-seq immune signature scoring
- UMAP dimensionality reduction
- Random Forest classification
- Feature importance analysis
- Correlation analysis
- Immune state modeling
- Pathway enrichment analysis
- Gene network visualization

---

## Technologies

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

## Biological Interpretation

The results support a model in which:

1. Tumor immune activation initiates cytotoxic anti-tumor responses  
2. Chronic stimulation induces immune checkpoint pathways  
3. Persistent checkpoint signaling leads to T-cell exhaustion  
4. This process contributes to **tumor immune escape**

Understanding these mechanisms may improve identification of tumors responsive to **immune checkpoint blockade therapies**.

---

## Author
Agata Gabara
Bioinformatics project exploring immune heterogeneity and immune escape mechanisms in lung cancer.
