# rct_generalizability_flatiron

## Introduction
The aim of this project is to reproduce landmark oncology randomized controlled trials (RCTs) and to assess their generalizability to patients in routine clinical practice. A total of 11 RCTs were reproduced across 4 different cancer types: advanced NSCLC, metastatic breast, metastaic prostate, and metastatic colorectal. 

A machine-learning (ML) survival model was constructed for each of the 4 cancers. Next, the ML models stratified patients into 3 survival risk groups. Landmark RCTs were then simulated for each risk group using inverse probability of treatment-weighted survival analyses.

Flatiron Health data was used to train and test the ML survival models and to reproduce the RCTs in-silico. 

## Notebooks
The project was coded in Python. See requirement.txt for necessary packages and versions to run Jupyter notebooks. 

There are 7 core notebooks for each cancer: 
1. data_wranging_tr: Data wranging of the training set
2. data_wranging_te: Data wrangling of the test set 
3. crude_model_build: Building ML survival models using a crude imputation strategy
4. cox_model_build: Building a standard Cox model inspired 
5. mice_gbm_build: Building gradient-boosted survival models with multiple imputation strategy 
6. discrim_performance: Plotting the time-dependent AUC for all ML models 
7. rtrials_wt3r_33c: Reproducing landmark clinical trials across 3 risk groups  

