# PM2.5 Concentration Forecasting (Delhi)

## Project Overview

- **Goal:** Explore, preprocess, and model historical PM2.5 concentration data to produce short-term forecasts for Delhi.
- **Scope:** Exploratory data analysis (EDA), time-series preprocessing, model selection and training (SARIMA implementation in the notebook), evaluation, and report generation.

## Data

-- **Primary dataset:** data/delhi_aqi.csv (contains PM2.5 measurements)
-- **Notes:** Inspect the CSV to identify the timestamp column and the PM2.5 measurement column, plus any additional features or metadata.

## Repository Structure

```
pm2.5_concentration/
├─ data/
│  └─ delhi_aqi.csv        # primary dataset (PM2.5 measurements)
├─ Notebooks/
│  ├─ EDA _preprocessing.ipynb
│  └─ model_sarima.ipynb    # model development and forecasting
├─ images/                  # plots and visual assets
├─ reports/                 # exported reports and tables
├─ requirements.txt         # Python dependencies
├─ README.md
└─ .gitignore
```

Links:

- data: [data/delhi_aqi.csv](data/delhi_aqi.csv)
- notebooks: [Notebooks/EDA _preprocessing.ipynb](Notebooks/EDA%20_preprocessing.ipynb), [Notebooks/model_sarima.ipynb](Notebooks/model_sarima.ipynb)


## Requirements

- Python 3.9 or newer
- Recommended: create a virtual environment to isolate dependencies.

## Quick Setup (Windows PowerShell)

1. Create and activate a virtual environment:

```powershell
python -m venv .venv
Set-ExecutionPolicy -Scope Process -ExecutionPolicy RemoteSigned
& .venv\Scripts\Activate.ps1
```

2. Install required packages:

```powershell
pip install -r requirements.txt
```

3. Start Jupyter Lab/Notebook and run notebooks in order:

```powershell
jupyter lab
```

## Usage Guide

1. Run the EDA & Preprocessing notebook to inspect the data, handle missing values/outliers, and prepare the time series for modeling.
2. Run the Model SARIMA notebook to:
	 - Analyze seasonality and stationarity;
	 - Select appropriate SARIMA parameters;
	 - Train, validate, and produce forecasts.
3. Output artifacts (plots, CSVs, figures) are saved to `images/` and/or `reports/` — check notebooks for exact export paths.

## Reproducibility

- Ensure versions in `requirements.txt` are installed to reproduce results.
- Run notebooks in the sequence: EDA → Model. For automation, convert notebooks to scripts using `nbconvert` or write a driver script.

## Results & Report

- Final plots and evaluation tables are available under `images/` and `reports/`.
- `main.tex` is provided to compile the formal report (use `pdflatex` or `xelatex`).

## Suggested Extensions

- Experiment with additional forecasting approaches: Prophet, LSTM/GRU, or tree-based models with lag features (e.g., XGBoost).
- Evaluate multi-step forecasting performance and compare metrics such as MAE, RMSE, and MAPE.

## Contributing

- Open an issue for discussion or submit a pull request to propose new models, preprocessing steps, or visualizations.
