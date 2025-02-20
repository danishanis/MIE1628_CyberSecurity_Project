# Cyber Security: Malware Prediction Project
Cyber security - Microsoft Malware Prediction

## Business Problem

This project aims to analyze Microsoft’s Malware Prediction dataset from Kaggle using a Binary Classifier developed in Apache Spark. The objective is to be able to predict whether a malware can occur in a device or not based on the provided features. Precise classification of devices at risk of malware can allow users and manufacturers to make better business decisions about how to increase the availability of their device with minimum maintenance and expenditure. 

A logistic regression algorithm was developed for the purpose, and its classification performance was compared with other supervised learning algorithms like Gradient Boosting and Random Forest. Additionally, the overall performance of the system was enhanced by efficient feature engineering, grid search and cross validation. As a metric for model performance evaluation, area under the receiver operator characteristic curve was used to discriminate between models. A PCA-based dimensionality reduction in Scala has been seprately performed on a [breast cancer classification](https://github.com/danishanis/PCA_in_Scala_for_Breast_Cancer_Classification) case study

## Introduction

The internet has grown exponentially with Microsoft as the primary OS for both personal and business computers and with that has grown the malware industry. An estimated 350k malwares are detected by Microsoft daily, assessing the current antivirus market share to be around US$3.7 Billion. Below we can see the rapid increase in these numbers, thus making malware detection a crucial problem for the industry.

![Annual Malware Growth](https://user-images.githubusercontent.com/51137481/71354493-1c403900-254a-11ea-9881-8889f5f3e3bb.png)

Given the need to build a more robust anti-malware system while not compromising on customer needs, it will be beneficial for the makers to be able to gauge the likelihood of a malware attack based on the different factors.

## Dataset

Microsoft has collected a huge amount of data to challenge Kaggle’s data science com-munity for a suitable solution.

•	[Kaggle Microsoft Malware Prediciton Competetion](https://www.kaggle.com/c/microsoft-malware-prediction)

•	[Training & Testing Data](https://www.kaggle.com/c/microsoft-malware-prediction/data)

Each observation contains 81 features/characteristics about Windows devices such as if the device as an anti-virus installed, if it is protected, presence of a smart screen, optical disk drive etc. Every feature has 89,215 observations. The target label visible only in the training dataset shows whether malware was detected or not with ‘1’ meaning yes and ‘0’ meaning no.

## Target Variable Distribution

As a supervised binary classification problem, the target variable indicates either presence of malware with ‘1’ or no malware with ‘0’. the business use case aims at allowing users and manufacturers to make better decisions with regards to their Microsoft devices. Therefore, also visualized are the top 10 countries that the data was procured from and observed that Congo and Lithuania had the highest number of malware detections.

![Target Variable Distribution](https://user-images.githubusercontent.com/51137481/71355339-c1f4a780-254c-11ea-8920-f4ffa767b1ab.png)

## Methodology 

![Methodology](https://user-images.githubusercontent.com/51137481/71355727-ef8e2080-254d-11ea-956f-a9a5c8b882ec.png)

## Model Improvement

Used Grid Search by conducting both train validation split and cross validation. Parameters parallelized in grid search included Regularization Parameter, Max Iterations, Various Threshold values, Fit intercept and Elastic Net Parameter. There was a total of 28 hyperparameter combinations with k = 3 folds resulting in 84 runs.

• Elastic Net Parameter specifies the mix of L1 and L2 regularization. If this is low, it indicates no regularization is required.

• Fit Intercept determines whether to fit the intercept or not.

• Max Iterations is the number of iterations over the data before stopping.

• Regularization Parameter is the weight given to the regularization term. If this is low, there is no regularization required.

• Threshold helps us control the number of false positives and false negatives.

## Model Evaluation & Results

We obtained an AUROC of 65% for the training set and 64% for the test set. the baseline logistic regression model was compared against Gradient Boosting and Random Forest models. The choice of alternate models was inspired by kernels and case studies on the Kaggle competition page. Most participants achieved slightly better results with techniques like gradient boosting, random forest, decision trees etc. as compared to logistic regression. When we noticed that the classification accuracy isn’t majorly affected by tweaking hyperparameters, feature engineering was advocated to see if it improves results further. We noticed a significant improvement which led us to the conclusion that with proper feature engineering, hyperparameter tuning and scaling, Logistic Regression outperforms the other models. 

![AUROC Results](https://user-images.githubusercontent.com/51137481/71355885-72af7680-254e-11ea-88fd-4e785f14f44a.png)
