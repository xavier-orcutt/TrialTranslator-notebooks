# TrialTranslator-notebooks

## Introduction
This repository contains Jupyter Notebooks demonstrating data cleaning, machine learning (ML) model development, and trial emulation for the TrialTranslator framework. 

TrialTranslator is a framework designed to expose heterogenity of treatment effects among real-world oncology patients by emulating landmark Phase III RCTs across prognostic phenotypes identified through a ML algorithm. A total of 11 RCTs were emulated across 4 different cancer types: advanced NSCLC, metastatic breast, metastatic prostate, and metastatic colorectal. 

The framework operates in two steps. First, a ML survival model was constructed for each of the 4 cancers, allowing for individual patient mortality risk prediction at the time of metastatic diagnosis. Second, patients meeting the elgibility criteria for the RCTs of interest were stratified into one of three phenotypes (low, medium, and high risk) using ML models. Survival analysis was the performed, with metrics such as restricted mean survival time and median overall survival esetimated using inverse probabiliy of treatment weighted Kaplan-Meier survival curves. The Flatiron Health database was used both for training the ML models and conducting the emulated trials. 

## Notebooks
The project was coded in Python. The required packaged can be found in the requirement.txt file.

There are 4 cancer specific directories (lung, breast, colorectal, and prostate). Each contains the following notebooks: 
1. data_wranging_tr: Data wranging of the training set
2. data_wranging_te: Data wrangling of the test set 
3. crude_model_build: Building various ML survival models using a median imputation strategy
4. cox_model_build: Building a standard Cox model inspired by retrospective study
5. mice_gbm_build: Building a gradient boosting survival model with MICE
6. patient_risk_score: calculating patient risk scores using GBM 
7. final_model_build: A final GBM was trained over the complete dataset for deployment in the webtool
8. rtrials_wt3r_33c_surv_metrics: Survival metrics (HR, RMST, mOS) for landmark clinical trials across phenotypes using key inclusion criteria
9. strials_wt3r_33c_surv_metrics: Survival metrics (HR, RMST, mOS) for landmark clinical trials across phenotypes using strict inclusion criteria
10. rtrials_wt3r_33c_dc_surv_metrics: Survival metrics (HR, RMST, mOS) for landmark clinical trials across phenotypes using while ensuring appropriate upfront dosing of chemotherapeutics 

## Website
Visit [here](https://trialtranslator.com) for the website version of this project. 
