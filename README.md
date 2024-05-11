AIDS Virus Infection Prediction
This repository contains code for predicting AIDS virus infection based on healthcare statistics and categorical information about patients.

Dataset
The dataset used for this project contains various attributes such as patient demographics, medical history, treatment history, and laboratory results. It was initially published in 1996 and serves as a valuable resource for predictive modeling and exploratory data analysis in the field of healthcare analytics and epidemiology.

Attribute Information
time: Time to failure or censoring
trt: Treatment indicator (0 = ZDV only; 1 = ZDV + ddI, 2 = ZDV + Zal, 3 = ddI only)
age: Age (years) at baseline
wtkg: Weight (kg) at baseline
hemo: Hemophilia (0=no, 1=yes)
homo: Homosexual activity (0=no, 1=yes)
drugs: History of IV drug use (0=no, 1=yes)
karnof: Karnofsky score (on a scale of 0-100)
oprior: Non-ZDV antiretroviral therapy pre-175 (0=no, 1=yes)
z30: ZDV in the 30 days prior to 175 (0=no, 1=yes)
preanti: Days pre-175 anti-retroviral therapy
race: Race (0=White, 1=non-white)
gender: Gender (0=F, 1=M)
str2: Antiretroviral history (0=naive, 1=experienced)
strat: Antiretroviral history stratification (1='Antiretroviral Naive',2='> 1 but <= 52 weeks of prior antiretroviral therapy',3='> 52 weeks)
symptom: Symptomatic indicator (0=asymp, 1=symp)
treat: Treatment indicator (0=ZDV only, 1=others)
offtrt: Indicator of off-trt before 96+/-5 weeks (0=no,1=yes)
cd40: CD4 at baseline
cd420: CD4 at 20+/-5 weeks
cd80: CD8 at baseline
cd820: CD8 at 20+/-5 weeks
infected: Is infected with AIDS (0=No, 1=Yes)
Code
The code provided in this repository implements logistic regression models for predicting AIDS virus infection based on the dataset provided. The code is written in Python and uses libraries such as Pandas, NumPy, Seaborn, Matplotlib, and scikit-learn for data manipulation, visualization, and modeling.

Usage
To run the code:

Clone this repository to your local machine.
Install the required dependencies by running pip install -r requirements.txt.
Run the aids_virus_infection_prediction.py script.
