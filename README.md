# Robust Conformal Prediction under Distributional Shift

## Overview
Conformal prediction offers finite-sample uncertainty guarantees, but these
guarantees rely on exchangeability between calibration and test data. Under
distributional shift, classical conformal prediction can severely under-cover.

This project empirically evaluates robust and fine-grained conformal inference
methods under controlled covariate shift scenarios, focusing on the trade-off
between coverage validity and interval efficiency.

---

## Methods Implemented
- Split Conformal Prediction (CP)
- Weighted Conformal Prediction (WCP)
- Robust Conformal Prediction (RCP)
- Weighted Robust CP (WRCP)
- Clustered (Fine-Grained) RCP

Weighted methods estimate importance weights via a domain classifier, while
robust methods inflate calibration thresholds using a robustness parameter ρ.
Clustered methods perform local calibration to adapt to heterogeneous shift.

---

## Experimental Design
- Dataset: Communities & Crime (normalized)
- Target coverage: 90%
- Mild and severe covariate shift regimes
- 30 repeated trials per setting
- Evaluation metrics:
  - Empirical coverage
  - Average interval length
  - Binwise conditional coverage

---

## Key Findings
- Classical CP fails under both mild and severe shift due to broken exchangeability.
- Global robustness improves coverage but produces overly wide intervals.
- Weight-based methods are highly conservative and sensitive to weight quality.
- Fine-grained (clustered) conformal inference achieves near-nominal coverage
  with substantially shorter intervals, especially under heterogeneous shift.

---

## Project Structure
robust-conformal-inference/
│── robust-conformal-inference.ipynb
├── crime_data_normalied.xlsx
├── report/
│ └── Final_Project_Report.pdf
└── README.md


---

## Academic Context
This project was completed as part of a graduate-level course in Statistical
Learning for Data Science and is inspired by:
Ai & Ren (2024), *Not All Distributional Shifts Are Equal: Fine-Grained Robust
Conformal Inference*.

---

## License
MIT License
