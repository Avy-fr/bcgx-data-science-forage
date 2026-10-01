# PowerCo Customer Churn Analysis

**BCG X Data Science Job Simulation on Forage**

This repository presents my completed work for the PowerCo customer-churn case in the **BCG X Data Science Job Simulation hosted on Forage**. The project progresses from business framing and exploratory analysis through feature engineering, predictive modeling, and an executive summary.

> **Important disclosure:** This is an educational job-simulation project. It does **not** represent employment, an internship, or client work performed for BCG X or PowerCo. The simulation-provided datasets, starter templates, and instructional materials are not redistributed in this repository.

## Simulation tasks

| Task | Focus | Portfolio deliverable |
|---|---|---|
| **Task 1** | Business understanding and data requirements | [`docs/task_01_business_understanding.md`](docs/task_01_business_understanding.md) |
| **Task 2** | Exploratory data analysis | [`notebooks/task_02_exploratory_data_analysis.ipynb`](notebooks/task_02_exploratory_data_analysis.ipynb) |
| **Task 3** | Feature engineering | [`notebooks/task_03_feature_engineering.ipynb`](notebooks/task_03_feature_engineering.ipynb) |
| **Task 4** | Random Forest churn modeling | [`notebooks/task_04_predictive_modeling.ipynb`](notebooks/task_04_predictive_modeling.ipynb) |
| **Task 5** | Executive stakeholder summary | [`reports/task_05_executive_summary.pdf`](reports/task_05_executive_summary.pdf) |

## Business question

The simulation asks whether **price sensitivity is a major driver of SME customer churn** and how data science can help PowerCo identify customers at risk of leaving.

The analysis treats price sensitivity as a hypothesis to test rather than a conclusion to prove.

## Key findings

- The customer dataset contains **14,606 customers**.
- Approximately **9.7%** of customers churned, making the target strongly imbalanced.
- Some peak and mid-peak price components are higher among churned customers, while off-peak variable prices are very similar between churned and retained customers.
- Churned customers show slightly shorter average tenure and substantially lower average consumption in the exploratory analysis.
- The engineered modeling dataset contains **70 columns**, with no missing values, duplicate customer IDs, or infinite numeric values in the completed run.
- The Random Forest model reaches **90.3% accuracy**, but churn recall is only **5.46%**.
- The model identifies **20 of 366 actual churners** in the test set.
- The top model features are dominated by consumption, margin, meter-rent, power, and customer-activity variables rather than price-related features.

## Model performance

| Metric | Result |
|---|---:|
| Accuracy | 90.31% |
| Precision | 71.43% |
| Recall | 5.46% |
| F1 score | 10.15% |
| ROC-AUC | 66.49% |

### Confusion matrix

| | Predicted retained | Predicted churned |
|---|---:|---:|
| **Actual retained** | 3,278 | 8 |
| **Actual churned** | 346 | 20 |

## Business interpretation

The high accuracy is misleading because the model misses most churners. For a retention use case, improving recall is more important than optimizing headline accuracy alone.

The analysis also provides limited support for using broad price discounts as the default churn intervention. A more defensible next step is to improve churn detection, combine customer-level risk with commercial value, and test targeted retention offers.

## Repository structure

```text
powerco-customer-churn-analysis/
├── README.md
├── docs/
│   └── task_01_business_understanding.md
├── notebooks/
│   ├── task_02_exploratory_data_analysis.ipynb
│   ├── task_03_feature_engineering.ipynb
│   └── task_04_predictive_modeling.ipynb
├── reports/
│   └── task_05_executive_summary.pdf
├── data/
│   ├── README.md
│   ├── raw/
│   └── processed/
├── requirements.txt
└── .gitignore
```

## Technology

- Python
- pandas
- NumPy
- Matplotlib
- seaborn
- scikit-learn
- Jupyter Notebook

## Reproducing the analysis

The simulation datasets are intentionally omitted from the public repository. If you have authorized access to the Forage materials, place the required files according to [`data/README.md`](data/README.md), install the dependencies, and run the notebooks in task order.

```bash
pip install -r requirements.txt
```

## Limitations

- The target is highly imbalanced, so accuracy is not an adequate standalone performance measure.
- The Random Forest result is a baseline model from the simulation workflow rather than a production-ready churn system.
- The reported model metrics are the outputs from the completed simulation run; small differences may occur when rerunning under different library versions.
- Feature importance is predictive and model-specific; it should not be interpreted as causal evidence.
- Further work should consider class-imbalance treatment, threshold tuning, stronger validation, probability calibration, and controlled testing of retention interventions.
