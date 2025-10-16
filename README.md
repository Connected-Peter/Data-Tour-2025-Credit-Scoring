# Data-Tour-2025-Credit-Scoring
Credit Default Prediction Challenge – DataTour 2025 by Peter Osuolale
# DataTour 2025 - Credit Scoring (Team: GTF)

**Project:** National phase of DataTour 2025 — Credit default prediction based on historical loan data.

## Context
Access to credit is a key lever of economic development. This project aims to build models to predict loan default (flag = 1) vs correct repayment (flag = 0) using customers' credit histories.
Approaches include tabular ML models (LightGBM, CatBoost, XGBoost) and sequential neural models (LSTM/Transformer) on payment sequences.

## Dataset Notes
- Each row = a credit product for a customer.
- Key columns: `id`, `flag`, `rn`, `pre_*` (loan metadata), `enc_paym_*` (payment sequence), categorical encoders like `enc_loans_credit_type`, flags `pclose_flag` / `fclose_flag`, etc.
- Evaluation metric: ROC AUC.
- Submission format: `.parquet` with columns `id`, `target`.