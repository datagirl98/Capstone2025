### Hospitalization costs

Patricia Polchow

#### Executive summary: This project leverages data from 55K records across multiple hospitals and multiple conditons. Through data analysis I seek to understand key factors that influence billing amount across medical conditions, location, patient age and insurance plan

**Project overview and goals:** The goal of this project is to identify data elements that can help preduct Billing amounts. We will be approaching this project as a multi-classification project to leverage the datas elements in our data set. We will compare 4-5 models' performances to select the best performing at predicting billing amount. After drawing insights and analysing results we will share elements that can help predict bill amount given a set of data values.

**Findings:** After comparing Linear Regression, Ridge Regression, Lasso Regression, Elastic Net Regression models we could see that all models were performing identically with very poor R2 values at close to or less than zero. This tells us that none of the models are explaining variance better than just predicting the mean. We did see that Lasso and Elastic Net slightly outperform the other models, but the gain was minimal. We decided to change our approach and convert this problem to a multi-classification problem by categrizing billing amounts as low, medium and high. We used XGBoost and integrated SMOTE into the pipeline to balance the training set before traning the XGBoost model. The model grouped the bill amounts into 3 classes: Class 0 bill amount <= $1000, medium was bill amount <=$5000 and categorized as (class 1) and anything above $5000 was categorized as High (class 2). The results of this model showed us that there is a severe class imbalance in class 1 where we have too few data samples. The recommendation is to apply more advanced machine learning techniques that can fine tune features.

📊 Evaluation Breakdown
Class	Label	Precision	Recall	F1	Support
0	Low	0.92	0.78	0.84	10,188
1	Medium	0.01	0.07	0.02	85
2	High	0.10	0.24	0.14	827

### Rationale
The cost of health care is highly varied throughout the healthcare industry. Understanding of driving factors helps both patients and healthcare companies. 

#### Research Question
Are there key factors that can help us predict healthcare costs?


#### Data Sources
The healthcare Dataset found in Kaggle at 
https://www.kaggle.com/datasets/prasad22/healthcare-dataset/data

#### Methodology
Regression analysis, specifically:
'Linear Regression'
'Ridge Regression'
'Lasso Regression'
'Elastic Net Regression'


#### Results
Still in progress

#### Next steps
Meet with advisor and get more guidance on path forward.

#### Outline of project

- https://github.com/datagirl98/Capstone2025.git)
  
##### Contact and Further Information
