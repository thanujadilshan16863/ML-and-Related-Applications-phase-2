# Machine Learning and Related Applications

**Student ID:** `KIC-BSCCSAI-251P-050`  
**Paper Under Review:** Rizk-Allah et al. (2024), *Explainable AI and optimized solar power generation forecasting model based on environmental conditions*, PLOS ONE 19(10): e0308002.

---

## 📁 Repository Overview

This repository contains reproducible code artifacts, datasets, and experiment outputs for the coursework across all phases:

```text
├── KIC-BSCCSAI-251P-050-phase2-appendix.ipynb   # Phase 2: Baseline modeling & benchmark notebook
├── Plant_1_Generation_Data.csv                  # Solar Plant 1 inverter power generation data
├── Plant_1_Weather_Sensor_Data.csv              # Solar Plant 1 weather sensor readings
├── Plant_2_Generation_Data.csv                  # Solar Plant 2 inverter power generation data
├── Plant_2_Weather_Sensor_Data.csv              # Solar Plant 2 weather sensor readings
├── outputs/                                     # Phase 2 evaluation metric tables and figures
│   ├── expA_... to expD_...                     # Benchmark evaluation tables (CSV)
│   ├── fig1_... to fig4_...                     # Visualization figures
│   └── summary_vs_paper.csv
└── phase3/                                      # Phase 3 technical appendix & reproducible outputs
    ├── KIC-BSCCSAI-251P-050-phase3-appendix.ipynb # Documented, reproducible Phase 3 notebook
    └── outputs/                                 # Phase 3 metrics, figures, and tables
        ├── results.json                         # Machine-readable metrics, grids & confidence intervals
        ├── fig_p3_intervals.png                 # Publication figures (Figures 1-4)
        ├── fig_p3_paper_table.png
        ├── fig_p3_skill.png
        ├── fig_p3_stress.png
        └── e1_... to e9_...                     # Exported CSV data tables (e1-e9)
```

---

## 🔬 Coursework Phases Summary

### Phase 1: Conceptual Mapping (Deconstruction)
- Standardized ML problem formulation (target: AC power, continuous regression).
- Methodological critique of the paper's optimization and deep neural architectures.
- Rigorous data pipeline audit (identifying zero-filtering caveats and inverter-level distributions).

### Phase 2: Technical Application (Baseline Implementation)
- Reproducible benchmark baselines (Linear Regression, Ridge, Decision Trees, Random Forest, HistGradientBoosting, MLP).
- Chronological vs. random 80/20 train/test split contrast demonstrating temporal data leakage.
- Multi-horizon evaluation ($h = 0$, $h = 1$, $h = 4$) and stress tests on dimensionality, noise, and cross-plant transfer.

### Phase 3: The Technical Review Report & Implementation
- **Technical Summary & Critique:** Deep analysis of the paper's methodology, validation protocol, metrics, and reported anomalies (e.g., negative MAE claim in the paper).
- **LSTM Proxy Benchmark:** Re-implementation of the paper's architecture (24 units, Adam, 45 epochs) under identical hyperparameters.
- **Proposed Alternatives:**
  - *Alternative A (Deterministic):* Lag-feature Gradient Boosting with daylight filtering.
  - *Alternative B (Probabilistic):* Calibrated Conformal Quantile Regression delivering 90% prediction intervals.
- **Stress-Testing Suite:** Robustness testing under Gaussian noise corruption, noise feature explosion, simulated pyranometer outage, and sample scarcity.

---

## 🚀 Environment & Reproduction

### Prerequisites
- Python 3.10+
- Required libraries:
  ```bash
  pip install numpy pandas scikit-learn matplotlib torch ipython
  ```

### Running the Notebooks
Execute the notebooks sequentially in Jupyter Lab, VS Code, or Google Colab:
1. `KIC-BSCCSAI-251P-050-phase2-appendix.ipynb` (saves outputs to `outputs/`)
2. `phase3/KIC-BSCCSAI-251P-050-phase3-appendix.ipynb` (saves outputs to `phase3/outputs/`)
