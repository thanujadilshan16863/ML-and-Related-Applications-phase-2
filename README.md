# ML and Related Applications - Phase 2

This repository contains the dataset, experiment outputs, and Jupyter Notebook research code for **Phase 2 of Machine Learning and Related Applications** (`KIC-BSCCSAI-251P-050`).

## 📁 Repository Structure

```text
├── KIC-BSCCSAI-251P-050-phase2-appendix.ipynb   # Complete analysis, modeling, and benchmark experiments
├── Plant_1_Generation_Data.csv                  # Solar Plant 1 inverter power generation data
├── Plant_1_Weather_Sensor_Data.csv              # Solar Plant 1 weather sensor readings
├── Plant_2_Generation_Data.csv                  # Solar Plant 2 inverter power generation data
├── Plant_2_Weather_Sensor_Data.csv              # Solar Plant 2 weather sensor readings
├── outputs/                                     # Generated evaluation tables and visualization figures
│   ├── fig1_days_lost.png
│   ├── fig2_test_predictions.png
│   ├── fig3_stress.png
│   ├── fig4_vs_paper.png
│   ├── expA_random_split_paper_table.csv
│   ├── expB_per_inverter_chrono_vs_random.csv
│   ├── expC_bootstrap_h1.csv
│   ├── expC_plant1_h0.csv
│   ├── expC_plant1_h1.csv
│   ├── expC_plant1_h4.csv
│   ├── expD_dimensionality.csv
│   ├── expD_noise.csv
│   ├── expD_plant2_h0.csv
│   ├── expD_plant2_h1.csv
│   └── summary_vs_paper.csv
└── README.md
```

## 🔬 Overview & Experiments

The study benchmarks and stress-tests machine learning models (Ridge, Decision Trees, Random Forests, HistGradientBoosting, MLP, etc.) on solar power generation data:
- **Experiment A:** Random split replication and paper comparison table.
- **Experiment B:** Per-inverter chronological vs. random split validation.
- **Experiment C:** Horizon testing (h=0, h=1, h=4) and bootstrap validation on Plant 1.
- **Experiment D:** Plant 2 evaluations, dimensionality reduction tests, and input noise robustness testing.

## 🚀 Getting Started

### Prerequisites

- Python 3.10+
- Jupyter Notebook / JupyterLab
- Required libraries:
  ```bash
  pip install numpy pandas scikit-learn matplotlib
  ```

### Running the Notebook

Open `KIC-BSCCSAI-251P-050-phase2-appendix.ipynb` in your preferred notebook environment (Jupyter, VS Code, or Google Colab) and execute the cells sequentially. Outputs and figures will automatically be saved to the `outputs/` folder.
