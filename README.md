# Preparing for Future Pandemics Vaccine Needs

![Vaccine in doctors hands](images/vaccine_header_readme.jpg)

## Overview

This project aims to help health providers prepare for the vaccination needs for future pandemics. From community clinics to health care providers with hospitals and offices aross regions, they will need *KJHJKHSDJKH*. The goals are to understand the indicators for recieving pandemic vaccines and build a model that will predict those who will get a pandemic vaccine.

## Business Understanding

Healthcare providers need to know how many vaccines  purchase or request, depending on the national distribution plan, so that all patients who want a vaccine recieve one and will not collect a large surplus. To answer this question we are going to build a model trained on data of individuals who recieved the h1n1 vaccine, to use to predict individuals who will likely recieve a future pademic vaccination. While overall accuracy is important, because health care providers would rather have slightly more vaccines than needed, rahter than being short and not having vaccines for individuals that requested them, we will focus on achieveing a high recall score.


## Data Understanding
The data comes from an over 26,000 person phone survey conducted in 2010, a year after the H1N1 outbreak, in which participants were asked about receiving the H1N1 vaccine, the seasonal flu vaccine, opionons about vaccines, behaviors around transmitting illness, and demograpic information.The dataset now has 26707 rows (survey respondents), and 38 columns (vairiables including id and targets). It has 12 objects and 26 numeric indicators. Indicators related to behavioral questions are binary,indicators related to opinion questions are a five point scale, numerical and srtingindicators related to demographics are of varying numbers of response choices, amd respondent ID is a unique identifer. The targets are binary, 0 or 1. 'health_insurance', 'employment_industry', and 'employment_occupation' all have over 50% nulls. Other columns contain a small percentage of nulls.

## Data Exploration

Of all respondents, 21% received the H1N1 vaccine. Notably, this is far less than those that reported receiving the annual flu vaccine, at 47%. 38& of those that recieved the seasonal flu vaccine recieved the H1N1 vaccine, 7% who did not recieve the seasonal flu vaccine recieved the H1N1 vaccine. 

![H1N1 vaccine percent](images/####.jpg)
![Seasonal flu vaccine percent](images/####.jpg)

Which grouping of questions is a better indicator of liklihood to get a vaccine? Note that for 'opinion_h1n1_sick_from_vacc', the higher score is associated with a negative relationship to teh vaccine, so add (6 - 'opinion_h1n1_sick_from_vacc') in the opinion sum. 

![H1N1 vaccine percent by behaviroal scores sum ](images/####.jpg)
![H1N1 vaccine percent by opinion scores sum ](images/####.jpg)

The opinion sum had a larger difference in percent of those that received the vaccine between the lowest and highest opinion scores, than that of the lowest and highest behavioral score.


## Modelling
dummy
fsm

### Grid search with CV models

A logistic regression model gridsearch was run using he following parameters:
        
        lr_params = {
                      'ct__num_trans__num_impute__strategy' : ['mean', 'median'],
                      'lr__penalty' : ['l1', 'l2', 'elasticnet'],
                      'lr__C' : [100, 10, 1.0, 0.1, 0.01],
                      'lr__solver' : ['lbfgs', 'liblinear', 'saga'],
                      }
                      
 Results:
 * Best parameters
 
>       {'ct__num_trans__num_impute__strategy': 'median',
>       'lr__C': 0.01,
>       'lr__penalty': 'l2',
>       'lr__solver': 'lbfgs'}

* Best score
    > 0.7962

Recall:
* 0.7911079745942131
![Recall score logistic regression grid search](images/cm_log_reg.png)

## Evaluation


## Conclusion
