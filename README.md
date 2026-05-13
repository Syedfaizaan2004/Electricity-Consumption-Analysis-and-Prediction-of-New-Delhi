# Electricity Consumption Analysis and Prediction - New Delhi

This project analyzes Delhi electricity consumption data for 2022 and builds a machine learning model to predict total electricity consumption from date and time features.

The workflow covers raw data cleaning, exploratory data analysis, visual reporting, and prediction using a Random Forest Regressor.

## Project Structure

```text
.
├── Data/                         # Raw daily CSV files grouped by month
├── Model/                        # Trained prediction model
├── Notebook/                     # Jupyter notebooks for the project workflow
│   ├── data_cleaning.ipynb
│   ├── data_analysis.ipynb
│   └── prediction_model.ipynb
├── Output/                       # Cleaned datasets, summaries, and chart assets
│   ├── cleaned_data.csv
│   ├── daily_consumption.csv
│   ├── hourly_consumption.csv
│   ├── monthly_consumption.csv
│   └── report_assets/
└── Syed Faizaan Ahmad(06615002823) Electricity_Consumption_Analysis_and_Prediction_New_Delhi_Report.pdf
```

## Dataset

The raw data contains Delhi electricity board records from 2022, organized as daily CSV files by month. The cleaned dataset includes time-slot level consumption values and derived date features.

Main columns include:

- `TIMESLOT`
- `DELHI`
- `BRPL`
- `BYPL`
- `NDPL`
- `NDMC`
- `MES`
- `Date`
- `Year`
- `Month`
- `Day`
- `Day_Name`
- `Total_Consumption`

Dataset source noted in the project summary:

<https://www.kaggle.com/datasets/adityasartape/12-months-data-of-delhi-electricity-board-2022/data?select=delhi_dispatch>

## Notebooks

Run the notebooks in this order:

1. `Notebook/data_cleaning.ipynb` - combines and cleans raw monthly CSV files.
2. `Notebook/data_analysis.ipynb` - performs EDA and creates summary charts.
3. `Notebook/prediction_model.ipynb` - trains and evaluates the prediction model.

## Setup

Create and activate a virtual environment:

```bash
python3 -m venv .venv
source .venv/bin/activate
```

Install the main dependencies:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn joblib jupyter
```

Start Jupyter:

```bash
jupyter notebook
```

## Outputs

Generated outputs are stored in `Output/`, including:

- cleaned and aggregated CSV files
- chart images for reporting
- `report_summary.json` with project statistics, EDA results, and model metrics

The trained model is stored at:

```text
Model/electricity_prediction.pkl
```

## Model Summary

The prediction notebook trains a Random Forest Regressor using these features:

- `Year`
- `Month`
- `Day`
- `DayOfWeek`
- `Hour`

Target variable:

- `Total_Consumption`

Recorded model performance:

- MAE: `59.8854`
- MSE: `7488.4858`
- RMSE: `86.536`
- R2 score: `0.995306`

## Notes

- The `.venv/` directory is ignored by Git.
- Notebook checkpoints, Python caches, local OS files, and temporary plotting caches are ignored.
- Raw data, generated outputs, model artifacts, and the final PDF report are kept trackable by default because they are part of this project deliverable.
