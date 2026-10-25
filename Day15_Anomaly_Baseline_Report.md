# Day 15 — Anomaly Baseline + Mentor Review

## Deliverables
- `Day15_Anomaly_Baseline.ipynb`: runnable notebook.
- `anomaly_detection_results.csv`: row-level results and scores.
- `anomaly_method_summary.csv`: method summary.
- `plots/`: anomaly plots.
- `README_Day15.md`: usage, limitations, and mentor questions.

## Preliminary outputs
- IQR statistical baseline flagged 331 rows (10.10%).
- Isolation Forest flagged 89 rows (2.72%).
- Both methods flagged 60 rows (1.83%).
- Isolation Forest contamination was set to 0.03 as a working assumption, not a measured anomaly prevalence.

## Interpretation
These flags are candidate anomalies only. There are no verified anomaly labels in the dataset. `Potability` is not treated as an anomaly label. The dataset is static tabular data with synthetic timestamps, so this package demonstrates a repeatable pipeline rather than validated real-world underwater anomaly detection.

## Evaluation strategy proposed for mentor approval
1. Use the first 70% of rows in chronological order as training data.
2. Fit IQR bounds, median imputation, scaling, and Isolation Forest on training rows only.
3. Apply the fitted methods to later rows and report flagged counts, overlap, and candidate rows for review.
4. Do not report precision/recall/F1 until validated anomaly labels exist.
5. Confirm IQR multiplier, Isolation Forest contamination, split strategy, and domain validation procedure with mentor.
