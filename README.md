# MIE1628_CyberSecurity_Project
Cyber security - Microsoft Malware Prediction

## Business Problem

This project aims to analyze Microsoft’s Malware Prediction dataset from Kaggle using a Binary Classifier developed in Apache Spark. The objective is to be able to predict whether a malware can occur in a device or not based on the provided features. Precise classification of devices at risk of malware can allow users and manufacturers to make better business decisions about how to increase the availability of their device with minimum maintenance and expenditure. A logistic regression algorithm was developed for the purpose, and its classification performance was compared with other supervised learning algorithms like Gradient Boosting and Random Forest. 

Additionally, the overall performance of the system was enhanced by efficient feature engineering, grid search and cross validation. As a metric for model performance evaluation, area under the receiver operator characteristic curve was used to discriminate between models.

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

As a supervised binary classification problem, the target variable indicates either presence of malware with ‘1’ or no malware with ‘0’. the business use case aims at allowing users and manufacturers to make better decisions with regards to their Microsoft devices. Therefore, the team also visualized the top 10 countries that the data was procured from and observed that Congo and Lithuania had the highest number of malware detections.

![Target Variable Distribution](https://user-images.githubusercontent.com/51137481/71355339-c1f4a780-254c-11ea-8920-f4ffa767b1ab.png)
