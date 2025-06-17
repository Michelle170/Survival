README

This repository contains data and code for the study on Joint Modeling for Time-to-Fatigue Prediction with a Single Wearable Sensor Biomarker. The materials are organized by case study and analytical stage to support replication and further exploration.

Data Files

Case Study 1: Manual material handling/Supply insertion (MMH/SI) Tasks
- consv_sds.csv: Long-form data for longitudinal process.
- time_fixed_conservative.csv: Short-form data for survival process.

Case Study 2: Bottle Picking (BP) Tasks
- long_data4_r0.5.csv: Long-form data for longitudinal process.
- short_data4_r0.5.csv: Short-form data for survival process.

Analysis Scripts

Data Preprocessing and Feature Selection
- 0_data_preprocessing.Rmd
  Performs leave-two-subject-out cross-validation setup and candidate feature selection based on point-biserial correlation. 

Baseline Modeling and Evaluation
- 1_baseline_modeling_evaluation.Rmd
  Fits baseline survival models (e.g., Kaplan Meier, Cox) using time-fixed covariates only.
  Outputs predicted survival probabilities and evaluation metrics across folds.

Joint Modeling and Evaluation
- 2_joint_modelling_evaluation.Rmd
  Fits joint models with selected longitudinal features. Evaluates multiple model configurations based on:
  - lmeform (longitudinal submodel specification)
  - JM parameterization (e.g., value, slope, or both)
  - Prediction time points
Outputs predicted survival probabilities and performance metrics across folds.
