# heart-disease-classifications

This notebook looks into using various Python-based machine learning and data science libraries in an attempt to build a machine learning model capable of predicting whether or not someone has heart disease based on their medical attributes.

We're going to take the following approach:
1. Problem definition
2. Data
3. Evaluation
4. Features
5. Modelling

## Problem Definition

In a statement,
> Given clinical parameters about a patient, can we predict whether or not they have a heart disease?

## Data

The original data came from the Cleveland database from the UCI Machine Learning Repository. https://archive.ics.uci.edu/ml/datasets/heart+disease

There is also a version available on Kaggle. https://www.kaggle.com/ronitf/heart-disease-uci

## Evaluation

> Trying to reach 95% accuracy of predicting whether or not a patient has heart disease.

## Features

This is where we'll get different information about each of the features in our data.

**Data dictionary**

  1. age - age in years 
  2. sex - (1 = male; 0 = female) 
  3. cp - chest pain type 
      * 0: Typical angina: chest pain related decrease blood supply to the heart
      * 1: Atypical angina: chest pain not related to heart
      * 2: Non-anginal pain: typically esophageal spasms (non heart related)
      * 3: Asymptomatic: chest pain not showing signs of disease
  4. trestbps - resting blood pressure (in mm Hg on admission to the hospital)
      * anything above 130-140 is typically cause for concern
  5. chol - serum cholestoral in mg/dl 
      * serum = LDL + HDL + .2 * triglycerides
      * above 200 is cause for concern
  6. fbs - (fasting blood sugar > 120 mg/dl) (1 = true; 0 = false) 
      * '>126' mg/dL signals diabetes
  7. restecg - resting electrocardiographic results
      * 0: Nothing to note
      * 1: ST-T Wave abnormality
          - can range from mild symptoms to severe problems
          - signals non-normal heart beat
      * 2: Possible or definite left ventricular hypertrophy
          - Enlarged heart's main pumping chamber
  8. thalach - maximum heart rate achieved 
  9. exang - exercise induced angina (1 = yes; 0 = no) 
  10. oldpeak - ST depression induced by exercise relative to rest 
      * looks at stress of heart during excercise
      * unhealthy heart will stress more
  11. slope - the slope of the peak exercise ST segment
      * 0: Upsloping: better heart rate with excercise (uncommon)
      * 1: Flatsloping: minimal change (typical healthy heart)
      * 2: Downslopins: signs of unhealthy heart
  12. ca - number of major vessels (0-3) colored by flourosopy 
      * colored vessel means the doctor can see the blood passing through
