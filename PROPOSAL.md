


# Project Title

Using Bayesian Inferences and Statsmodels to observe predictors interactions relations and predict the likelihood of positive breast cancer diagnosis in women with breast tumors.
 
# Introduction 
`Breast cancer` is one of the major life-threatening diseases in the world today. But early diagnosis would ensure timely treatment and even recovery. Apart from medical procedures that help to identify cancer and the skit -learn library, techniques such as Bayesian inferences and stats modelling on linear models can also  be applied to predict the chance that a patient has the disease by analyzing their cell data. Furthermore, Bayesian inferences from the PYMC posterior distributions of generalized linear regression models can be made about how various parameters interact with each other. For instance, how does the texture of a tumor change as the fractal dimension of the tumor increases?  How does the compactness of the tumor relate to its texture? If the tumor is so smooth, how does that affect the chance of the patient being positive? Are there parameters that carry more importance than others? What would happen if we removed information about Area, Radius  and Perimeter of the tumor? Would the prediction be so different from the actual diagnosis? In this work, an attempt is made to answer all these questions and more derivatives by applying Bayesian Inference and informative statsmodel  to a data set on which a Logistic regression from the Scikit-Learn Library, a variation of linear models, was applied by Kaiser Moo, an experienced data enthusiast in data science. The performance metrics of the statsmodel are analyzed against those of Kaiser’s logistic regression model and disparities explained.
 
Inspired by Kaiser's goal of evaluating a prediction model, I had my project employ the statsmodel as well as Bayesian Inferences to predict the chance that a given set of characteristics evaluate to a probability which entails positive breast cancer diagnosis. Unlike Kaiser’s project, this project's primary goal is not to not  to classify a. It could be done at the end to compare my model’s accuracy to Kaiser’s logistic regression model. Rather, the project outputs probabilities between 0 and 1 inclusive with a probability of 0 indicating 0% likelihood  of having breast cancer and 1 representing 100% likelihood  of a patient having breast cancer. Since these predictions are probabilities, to determine whether that value is in the breast cancer category, a suitable threshold based on the data set, and the model  is used to draw the line such that if a probability is above it, that probability would evaluate to positive and to negative if below.

The following are the input features used in the course of my project Analysis.
```
 
1.      ID (patient ID)
2.      Name
3.      Radius (the distance from the center to the coreference of the tumor)
4.      Texture (standard deviation of gray-scale values)
5.      Perimeter (circumference of the tumor, approx. 
6.      Area
7.      Smoothness (local variation in radius lengths)
8.      Compactness
9.      Concavity (severity of concave portions of the contour)
10.     Symmetry
11.     Fractal dimension
12.     Age

```
The following are the highlights of what steps my project followed to arrive at the linear regression model with multiple predictors, where the predictors are the characteristics:
 
1.*Data Engineering*

Here `breastcancer.csv` is normalized into a workable format using NumPy and Pandas

2.*Data Splitting*

Here the cleaned data is split into ‘training set’  to be fed into statsmodel and `testing set` to later feed into the models to report their accuracy.

3. `Fitting to Logistic Regression` 
4. 
The data set has categorical actual outcomes. However, the outcomes of logistcic regression are not classifier classes. So instead of having a likelihood output of either 0 or 1, the logit sigmoid function is used to collapse the 1s and 0s into probability values between 0 and 1. This changes the question from does the patient with `xyz` tumor characteristics have breast cancer to what is thelilihood that patient `xyz` given certain parameters is diagnosed with breast cancer? 

4.`Bayesian Inferences on Multiple Predictors`

Bayesian Inferences of parameter interaction are made using `PYMC3` traces and models’ recall, accuracy precision scores are manually calculated.

5.`Analysis`

Answering project core questions and evaluating accurately the models and implications of findings.
 
 # Goal
The goal is to mine all sorts of interactions between  important parameters, control certain parameters and observe the changes in model performance, which the Kaiser’s project does not do. Who knows, maybe some parameters in the model add only insignificant weight thereby making the model overly complex.  A comparison of the accuracy of my Bayesian Linear regression model and stats models to that of Kaiser by answering questions like if the women predicted to not have breast cancer, how many were classified as not having breast cancer? Of the women predicted to have breast cancer, how many were classified as not having breast cancer? How accurate is the Statsmodel logit model for the data at hand overall? How much variation is explained by the model? What are the tradeoffs of choosing to predict cancer with Statsmodel  Logit model vs  Scikit-learn logistic regression vise-versa? Is there a way we can cut on the number of predictors based on the discovered relationships between parameters? What predictors Can be added to improve the accuracy of the model overall?
 
 # Purpose
The purpose of the research is not to just to compare the performance of a  Bayesian Generalized Linear regression and Stasmodels  to that of a  Skit-Learn logistic regression model, or merely discover meaningful interactions between parameters, but to provide insights into possible reasons certain predictive models are preferred over others for given tasks, and also highlight that even though some models perform better than others, still, the inferior models on that task may, or may not, provide insight about other aspects of the data in a way that the selected model does not. (NB: My assumption was Bayesian linear models and Statsmodels  are inferior to Skit-Learn library  logistic regression since they tend to overfit outliers, the project can confirm this too). For example, they can help us understand the actual effect that  tempering with individual parameters has on the outcome, if at all the given parameter does affect the outcome at all.

# Why this Project?
Knowledge about parameter interactions and the models’ accuracies are indispensable as any incorrect diagnosis, especially false negative diagnosis, presents a very high cost financially and emotionally to the patient and their relatives, of which my family and I have fallen victims of. It is, therefore, my hope that mining the behavior of Generalized Bayesian Linear regression models inspires criticism of other models currently employed and not employed in clinical diagnosis of breast cancer.
