# Data setup

The source datasets and starter materials were supplied through the **BCG X Data Science Job Simulation on Forage**. They are not included in this public portfolio package.

To rerun the notebooks with your own authorized copy of the simulation data, use the following local structure:

```text
data/
├── raw/
│   ├── client_data.csv
│   └── price_data.csv
└── processed/
    ├── clean_data_after_eda.csv
    └── data_for_predictions.csv
```

Notebook dependencies:

| Notebook | Required local files |
|---|---|
| Task 2 - Exploratory Data Analysis | `data/raw/client_data.csv`, `data/raw/price_data.csv` |
| Task 3 - Feature Engineering | `data/processed/clean_data_after_eda.csv`, `data/raw/price_data.csv` |
| Task 4 - Predictive Modeling | `data/processed/data_for_predictions.csv` |

The notebooks retain the executed outputs from the completed simulation workflow so the analysis can be reviewed without redistributing the underlying simulation datasets.
