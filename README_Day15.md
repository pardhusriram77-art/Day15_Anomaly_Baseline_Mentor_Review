# Day 15 — Anomaly Baseline + Mentor Review

## Files
- `Day15_Anomaly_Baseline.ipynb` — notebook implementing IQR and Isolation Forest.
- `anomaly_detection_results.csv` — row-level scores and flags.
- `anomaly_method_summary.csv` — flagged-row summary.
- `Day15_Anomaly_Baseline_Report.md` — preliminary results and evaluation plan.
- `plots/` — visualizations.

## Running the notebook
Place the source file `water_potability_temporal_synthetic.csv` in `../underwater_temporal_dataset/` relative to the notebook, or edit `DATA_PATH` in the first code cell.

## Critical limitation
Timestamps are synthetic and the dataset has no ground-truth anomaly labels. These are candidate anomalies for review, not confirmed sensor faults. Do not present them as validated real-time environmental findings.

## Mentor decisions requested
- Is the 70% chronological training split acceptable?
- Is IQR multiplier 1.5 acceptable as a baseline?
- Is Isolation Forest contamination 0.03 acceptable as a provisional setting?
- Can validated sensor thresholds or labeled anomalies be provided for meaningful evaluation?
