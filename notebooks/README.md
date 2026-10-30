# Notebook learning path

Run notebooks in numeric order from the repository root or from `notebooks/`; each notebook locates the project root. Install dependencies once: `python -m pip install -r requirements.txt`. Download the IEEE-CIS dataset and place the four CSV files in `data/01_raw/`. Notebooks 01 and 04 create ignored intermediate files. Model artifacts are saved under `models/`, and evaluation reports under `reports/`.

| Notebook | Purpose |
|---|---|
| 01 | Join transaction and identity tables |
| 02 | Validate schema, missingness, duplicates, time, and labels |
| 03 | Explore fraud prevalence and behavior |
| 04 | Create time-aware behavioral features |
| 05 | Fit an interpretable logistic-regression baseline |
| 06 | Compare candidate models using a temporal split |
| 07 | Evaluate ranking, calibration, errors, and threshold costs |
| 08 | Build and inspect risk scores and bands |
| 09 | Explain global and individual model behavior with SHAP |
| 10 | Compare approve/review/decline policies and review capacity |
| 11 | Inspect distribution change and delayed-label metrics |
| 12 | Load the artifact and score an engineered example |

## Interpretation

IEEE-CIS is a benchmark, not a live institution’s data. Cost, review capacity, and score-band values are placeholders. Model selection and threshold analysis reuse the same latest-20% validation window; treat the results as exploratory, not an unbiased final estimate. Before deployment, reserve a later untouched temporal test window, verify label maturity and cost assumptions, and implement point-in-time feature state.
