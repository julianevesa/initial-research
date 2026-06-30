# Urban Vulnerability Modeling — SDG Target 11.1 - 2022 Brazilian Census

The methodological strategy of this project consists of the automated pre-processing of 644 socioeconomic and territorial variables extracted from the 2022 Demographic Census (IBGE). The workflow comprises statistical auditing, the elimination of redundancies via Pearson correlation analysis, and Min-Max normalization, thereby structuring a clean database for the direct application of the K-Means clustering algorithm. Distinct from traditional approaches, this model foregoes dimensionality reduction techniques (such as PCA) to preserve analytical transparency and ensure the direct interpretability of urban deficits across municipalities.

---

## 📂 Repository Structure

The project is organized into logical stages, separating raw data integration from the statistical modeling phase:

```text
.
├── 1_DATA_MERGE/                  # Stage 1: Data Ingestion & Unification
│   ├── ACM_SP.csv                 # Raw/intermediate Census data tables
│   ├── ACM_SP2.csv                # Raw/intermediate Census data tables
│   ├── ACM_SP3.csv                # Raw/intermediate Census data tables
│   ├── ACM_basico_SP.csv          # Core IBGE control variables
│   ├── pop_favelas_m.csv          # Aggregated external population data for slums
│   └── BD_.ipynb                  # Jupyter Notebook for extraction, cleaning, and merging
│
├── 2_ANALYSIS_MODELING/           # Stage 2: Statistical Analysis & Modeling
│   ├── base_final_SP.csv          # Consolidated and treated dataset ready for modeling
│   └── AN_KMEANS.ipynb            # Jupyter Notebook executing K-Means clustering & profiling
│
├── requirements.txt               # Project dependencies and library versions
└── README.md                      # Main project documentation
