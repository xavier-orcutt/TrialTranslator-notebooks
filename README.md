# TrialTranslator

## Introduction
The aim of this project is expose heterogenity of treatment effect in real-world oncology patients by emulating Phase III RCTs across prognostic phenotypes identified through a a machine learnign algroithm. A total of 11 RCTs were reproduced across 4 different cancer types: advanced NSCLC, metastatic breast, metastaic prostate, and metastatic colorectal. 

A machine-learning survival model was constructed for each of the 4 cancers. Next, the ML models stratified patients into 3 mortality phenotype (low, medium, and high). Landmark RCTs were then emulated for each phenotype and survival metrics (eg., restricted mean survival time and median overall survival) were estimated by a inverse probabiliy of treatment weighted Kaplan-Meier survival curve. 

Flatiron Health data was used for both training the machine learning models and performing the emulated trials. 

## Notebooks
The project was coded in Python using Jupyter Notebooks. See requirement.txt for necessary packages and versions to run notebooks. 

Each cancer file has the following notebooks: 
1. data_wranging_tr: Data wranging of the training set
2. data_wranging_te: Data wrangling of the test set 
3. crude_model_build: Building ML survival models using a median imputation strategy
4. cox_model_build: Building a standard Cox model
5. mice_gbm_build: Building gradient-boosted survival models with multiple imputation strategy 
6. gbm_final_build: Building the final gradient-boosted survival model 
7. rtrials_wt3r_33c_surv_metrics: Survival metrics (HR, RMST, mOS) for landmark clinical trials across phenotypes using key inclusion criteria
8. strials_wt3r_33c_surv_metrics: Survival metrics (HR, RMST, mOS) for landmark clinical trials across phenotypes using strict inclusion criteria
9. rtrials_wt3r_33c_dc_surv_metrics: Survival metrics (HR, RMST, mOS) for landmark clinical trials across phenotypes using while ensuring appropriate upfront dosing of chemotherapeutics 

## Website
See [here](https://github.com/xavier-orcutt/TrialTranslator-webtool) for the website version of this project. 
