# TrialTranslator-notebooks

## Introduction
This repository contains Jupyter Notebooks demonstrating data cleaning, machine learning (ML) model development, and trial emulation for the TrialTranslator framework. 

TrialTranslator is a framework designed to expose heterogenity of treatment effects among real-world oncology patients by emulating landmark Phase III RCTs across prognostic phenotypes identified through a ML algorithm. A total of 11 RCTs were emulated across 4 different cancer types: advanced NSCLC, metastatic breast, metastatic prostate, and metastatic colorectal. 

The framework operates in two steps. First, a ML survival model was constructed for each of the 4 cancers, allowing for individual patient mortality risk prediction at the time of metastatic diagnosis. Second, patients meeting the elgibility criteria for the RCTs of interest were stratified into one of three phenotypes (low, medium, and high risk) using ML models. Survival analysis was the performed, with metrics such as restricted mean survival time and median overall survival esetimated using inverse probabiliy of treatment weighted Kaplan-Meier survival curves. The Flatiron Health database was used both for training the ML models and conducting the emulated trials. 

## Notebooks
The project was coded in Python, with all dependencies listed in the requirements.txt file.

The repository is organized into four cancer-specific directories (lung, breast, colorectal, and prostate). Each directory contains the following Jupyter notebooks:

1. Data Processing 
  * data_wrangling_tr: Preprocesses the training dataset
  * data_wrangling_te: Preprocesses the test dataset

2. Model Development
  * crude_model_build: Implements various machine learning survival models using median imputation
  * cox_model_build: Develops a standard Cox proportional hazards model based on retrospective study findings
  * mice_gbm_build: Implements a gradient boosting survival model with Multiple Imputation by Chained Equations (MICE)
  * final_model_build: Trains the gradient boosting survival model on the complete dataset for web tool deployment

3. Clinical Trial Analysis
  * rtrials_wt3r_33c_surv_metrics: Calculates survival metrics (Hazard Ratio, Restricted Mean Survival Time, median Overall Survival) for landmark clinical trials across phenotypes using key inclusion criteria
  * strials_wt3r_33c_surv_metrics: Computes survival metrics using strict inclusion criteria
  * rtrials_wt3r_33c_dc_surv_metrics: Evaluates survival metrics while accounting for appropriate initial chemotherapy dosing

## Website
Visit [here](https://trialtranslator.com) for the website version of this project. 
