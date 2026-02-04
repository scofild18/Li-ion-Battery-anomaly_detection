# Li-ion-Battery-: Anomaly Analysis Notebook

This repository contains a Jupyter Notebook that analyzes Li-ion battery time-series data to detect anomalies . The notebook is written to be reproducible, well-documented, and ready for publication on GitHub.



**Overview**
- **Goal:** Identify and explain anomalous behavior in Li-ion battery measurements 
- **Scope:** Data loading, preprocessing, exploratory data analysis (EDA), anomaly detection,  visualization, and results summary.

**What I did (step-by-step)**
- **Data ingestion:** Loaded the time-series battery dataset used for the analysis (see the first cells in the notebook for the exact source and file paths).
- **Preprocessing:** Cleaned timestamps, handled missing values, resampled or aligned time series, and engineered rolling metrics and calendar features (weekday, month, hour-of-day).
- **Exploratory Data Analysis (EDA):** Plotted distributions, time-series trends, and seasonal patterns to understand normal vs abnormal behavior.
- **Anomaly detection methods:** Implemented approaches including statistical thresholds, rolling z-score, and an unsupervised model such as Isolation Forest. Results from multiple methods are compared visually and quantitatively.
- **Temporal analysis:** Compared anomaly rates and battery metrics across time buckets (e.g., hour-of-day, day-of-week, month) to identify recurring patterns.
- **Visualization & interpretation:** Created clear charts (time-series with anomaly overlays, violin/box plots by time bucket) and summarized plausible causes for detected anomalies.

**Key findings (summary)**
- The notebook highlights where anomalies occur and which metrics are most sensitive. See the final notebook cells for a concise results table and recommended next steps.

**How to run this notebook**
1. Create and activate a Python environment (example using venv):

```bash
python -m venv .venv
# Windows PowerShell
.\.venv\Scripts\Activate.ps1
# macOS / Linux
source .venv/bin/activate
```

2. Install the typical packages used in the notebook (see the notebook for exact imports):

```bash
pip install pandas numpy matplotlib seaborn scikit-learn scipy statsmodels jupyter
```

3. Launch Jupyter and open the notebook:

```bash
jupyter notebook notebook_anomalyy_holidays.ipynb
```

4. Run the notebook cells in order. The notebook includes explanatory text; follow the run-order and rerun analysis cells if you change parameters.

**Dependencies**
- Typical libraries used: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`, `scipy`, `statsmodels`, and `jupyter`.
- If you prefer, create a `requirements.txt` with the exact versions shown at the top of the notebook.

**Reproducibility notes**
- The notebook documents the random seeds (when used) and any sampling or train/test splits. If you change dataset paths, update the first data-loading cell accordingly.

**Suggested next steps**
- Add a `requirements.txt` for exact versions.
- Add unit tests or a small script that runs key analysis functions headlessly (useful for CI).
- Add a short `notebooks/` README or convert critical analysis to a Python module for production monitoring.

**License & Citation**
- This repository does not include a license by default. Add a `LICENSE` file if you want to publish under a specific license (MIT, Apache-2.0, etc.).
- If you used a public dataset (e.g., NASA Li-ion battery dataset), cite the original dataset in the notebook and in this README.

---


