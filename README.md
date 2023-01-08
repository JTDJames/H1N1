# Preparing for Future Pandemics Vaccine Needs

## Overview

This project aims to help health providers prepare for the vaccination needs for future pandemics. From community clinics to health care providers with hospitals and offices aross regions, they will need *KJHJKHSDJKH*. The goals are to understand the indicators for recieving pandemic vaccines and build a model that will predict those who will get a pandemic vaccine.


![Vaccine in doctors hands](images/vaccine_header_readme.jpg)

# Business Understanding

Healthcare providers need to know how many vaccines  purchase or request, depending on the national distribution plan, so that all patients who want a vaccine recieve one and will not collect a large surplus. To answer this question we are going to build a model trained on data of individuals who recieved the h1n1 vaccine, to use to predict individuals who will likely recieve a future pademic vaccination. While overall accuracy is important, because health care providers would rather have slightly more vaccines than needed, rahter than being short and not having vaccines for individuals that requested them, we will focus on achieveing a high recall score.


## Data Understanding
The data comes from an over 26,000 person phone survey conducted in 2010, a year after the H1N1 outbreak, in which participants were asked about receiving the H1N1 vaccine, the seasonal flu vaccine, opionons about vaccines, behaviors around transmitting illness, and demograpic information.The dataset now has 26707 rows (survey respondents), and 38 columns (vairiables including id and targets). It has 12 objects and 26 numeric indicators. Indicators related to behavioral questions are binary,indicators related to opinion questions are a five point scale, numerical and srtingindicators related to demographics are of varying numbers of response choices, amd respondent ID is a unique identifer. The targets are binary, 0 or 1. 'health_insurance', 'employment_industry', and 'employment_occupation' all have over 50% nulls. Other columns contain a small percentage of nulls.

## Data Exploration


## Modelling


## Evaluation


## Conclusion
