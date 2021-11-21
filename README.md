# The Bayesian Perspective on Breast Cancer Diagnosis

## Aim

This project aims at drawing meaningful  `Bayesian Inferences` on a `Logistic Regression` Model for positive cancer diagnosis in patients with `tumors`.

![alt tag](https://github.com/Sheinstein/-Bayesian-Perspective-on-Breast-Cancer-Diagnosis/blob/main/bresast:c.png)
Image of a breast tumor


## Introduction 

`Breast cancer` is one of the major life-threatening diseases in the world today. But early diagnosis would ensure timely treatment and even recovery. Apart from medical procedures that help to identify cancer and the skit -learn library, techniques such as Bayesian inferences and stats modelling on linear models can also  be applied to predict the chance that a patient has the disease by analyzing their cell data. Furthermore, Bayesian inferences from the PYMC posterior distributions of generalized linear regression models can be made about how various parameters interact with each other. For instance, how does the texture of a tumor change as the fractal dimension of the tumor increases?  How does the compactness of the tumor relate to its texture? If the tumor is so smooth, how does that affect the chance of the patient being positive? Are there parameters that carry more importance than others? What would happen if we removed information about Area, Radius  and Perimeter of the tumor? Would the prediction be so different from the actual diagnosis? In this work, an attempt is made to answer all these questions and more derivatives by applying Bayesian Inference and informative statsmodel  to a data set on which a Logistic regression from the Scikit-Learn Library, a variation of linear models, was applied by Kaiser Moo, an experienced data enthusiast in data science. The performance metrics of the statsmodel are analyzed against those of Kaiser’s logistic regression model and disparities explained.

Inspired by Kaiser's goal of evaluating a prediction model, I had my project create variations of linear models called Bayesian linear regression and Statsmodel models to predict the chance that a given set of characteristics evaluate to a probability which entails positive breast cancer diagnosis. Unlike Kaiser’s project, this project is not a classification problem. It could be, which was done at the end to compare my model’s accuracy to Kaiser’s logistic regression model. Rather, the project outputs probabilities between 0 and 1 inclusive with a probability of 0 indicating 0% chance of having breast cancer and 1 representing 100% chance of a patient having breast cancer. Since these predictions are probabilities, to determine whether that value is in the breast cancer category, a suitable threshold based on the data set, is used to draw the line such that if a probability is above it, that probability would evaluate to positive and to negative if below.


##  Dataset

The  data set used in the project can be found on this `link`[https://github.com/Sheinstein/-Bayesian-Perspective-on-Breast-Cancer-Diagnosis/blob/main/breastcancer.csv]


## Jupyter Notebook

The notebook of the several experiments perfomed to can be found `here`[https://colab.research.google.com/drive/1hu6243boRjsLC4i54Dh1DEKeIOSHDcDl?usp=sharing]


## Related Work

Kaiser M. (2020). Predicting Breast Cancer Using Logistic Regression. Learning how to perform Explanatory Data Analysis, apply mean imputation, build a classification algorithm, and interpret the results. Ref: https://medium.com/swlh/predicting-breast-cancer-using-logistic-regression-3cbb796ab931
 

## Procedure

The following are the highlights of what steps the project followed to arrive at the regression model with multiple predictors, where the predictors are the characteristics:
 
### Data Engineering

Here `breastcancer.csv` is normalized into a workable format using NumPy and Pandas

### Data Splitting

Here the cleaned data is split into ‘training set’ to be fed into the PMC regression model and ‘Validation set’ to later feed into the models for checking how accurate they are.

### Training

The data set has categorical actual outcomes. However, the outcomes of linear regression are not classifier classes. So instead of having a likelihood output of either 0 or 1, the sigmoid function is used to collapse the 1s and 0s into probability values between 0 and 1. This changes the question from does the patient with `xyz` tumor characteristics have breast cancer to what is the chance that patient `xyz` given certain parameters has breast cancer? 

### Posterior Distribution Sampling

Bayesian Inferences of parameter interaction are made using PYMC traces and models’ recall, accuracy precision scores are manually calculated.


### Model Evaluation

Answering project core questions and evaluating accurately the models and implications of findings.
 

## Summary of Outcomes

The design of the various experiments answered all the questions the project aimed to answer. The Bayesian Inferences and statsmodels logistic models are not any less inaccurate than Moo’s sklearn’s logistic regression model. The former models are in fact handy as they readily inform the user of the goodness of fit of the model, thereby more or less implicitly warning the user on the likelihood of our model to be wrong. It would sure make a difference if all underlying models in the various breast cancer methods had this `feature` in them. So many patients would then know whether to take the news of diagnosis with or without a grain. 

If patients with tumors only differ in age and all else is the same, that does not affect the diagnosis outcomes so much according to the dataset. 

And if the standard deviation of the texture is large, the standard deviation of the smoothness is likely large too. However, if the smoothness is large, it is likely that the fractal dimension is small or vise versa. 

A tumor’s smoothness is the most important predictor in the diagnosis of cancer, followed by its fractal dimension, and then texture. All other non-multicollinear independent predictors do not weight as much in the diagnosis of cancer.


