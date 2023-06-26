# Classification-Project-Customer-Attrition-Case
Context
This project is a Supervised Machine Learning which aims to analyze customer churn, identify key indicators, and develop strategies for customer retention. By analyzing data variables and using various techniques, we aim to predict and mitigate customer churn.
Procedure
The file is going to document the steps and procedure used to complete this project in every step of the way. Below are the steps folowed to achieve the aim of the project.

Steps
Data Collection: The Telco customer data is collected from the provided sources, including the LP2_Telco_churn_first_3000 table in a SQL Server database and the LP2_Telco-churn-last-2000.csv and Telco-churn-second-2000.xlsx files. This data contains information about customer demographics, services subscribed, payment methods, and churn status.

Data Loading: The collected data is loaded into the code and transformed into a suitable format for analysis. The pyodbc package is used to connect to the SQL Server database and fetch data from the LP2_Telco_churn_first_3000 table. The data from the CSV and Excel files is read using the pandas library and concatenated with the SQL data to create a comprehensive dataset.

Data Evaluation (EDA): Exploratory data analysis is performed to gain insights into the dataset. This includes summarizing the data, checking for duplicates, handling missing values, and performing univariate and bivariate analyses. The pandas, numpy, matplotlib, and seaborn libraries are utilized for data manipulation and visualization.

Data Processing and Engineering: Data processing steps are applied to clean and preprocess the dataset. This involves handling missing values, transforming categorical variables, and creating new features if necessary. The dataset is prepared for further analysis using techniques from the pandas library.

Hypothesis Testing: Hypotheses related to customer churn are formulated and tested using statistical methods. The scipy library is used to perform hypothesis tests such as the Chi-Square Test of Independence and t-test. The significance of factors such as gender, internet service type, tenure, and payment method on customer churn is evaluated.

Answering Questions with Visualizations: Key questions related to customer churn are answered using visualizations. The matplotlib and seaborn libraries are employed to create informative plots and charts that illustrate the relationships between variables and churn.

Power BI Deployment: The analysis and visualizations were deployed in Power BI for interactive exploration and sharing with stakeholders. The insights gained from the analysis were presented using Power BI's dashboarding and reporting capabilities.

Balancing Dataset:To address class imbalance in the training set, the SMOTETomek technique is used to oversample the minority class and undersample the majority class. The class distribution is checked before and after balancing.

Train and Evaluate Four Models: Several machine learning models are trained and evaluated using both the imbalanced and balanced datasets. The models include Logistic Regression, Decision Tree, Random Forest, Gradient Boosting, AdaBoost, SVM, KNN, Naive Bayes, XGBoost, LightGBM, and CatBoost. Classification reports are generated for each model, and the F1-score is used as the evaluation metric.

Evaluate Chosen Model: The best-performing model from the previous step is further evaluated and fine-tuned if necessary. Confusion matrices are generated for each model to visualize the performance in terms of true positives, true negatives, false positives, and false negatives.

Advance Model Improvement: GridSearchCV is used to perform hyperparameter tuning for selected models. The best-tuned models and their parameters are obtained, and predictions are made using the best models.

Future Predictions: The trained and validated model can be used to make predictions on new, unseen data. This allows businesses to forecast customer churn and take proactive measures to retain customers. The model can be deployed in production to continuously monitor and predict customer churn.

Installation
To run the code in this repository, you need to install the following Python packages:

pyodbc
sqlalchemy
lightgbm
catboost
python-dotenv
pandas
numpy
matplotlib
seaborn
scipy
Packages
import sqlalchemy as sa
import pyodbc
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
from scipy.stats import chi2_contingency
from scipy.stats import ttest_ind
from sklearn.linear_model import LogisticRegression
from sklearn.tree import DecisionTreeClassifier
from sklearn.ensemble import RandomForestClassifier, GradientBoostingClassifier, AdaBoostClassifier
from sklearn.svm import SVC
from sklearn.neighbors import KNeighborsClassifier
from sklearn.naive_bayes import GaussianNB
from xgboost import XGBClassifier
from lightgbm import LGBMClassifier
from catboost import CatBoostClassifier
from sklearn.metrics import precision_score, recall_score, f1_score, roc_auc_score
Conclusion
Predicting customer churn in the Telco industry is crucial for businesses to identify at-risk customers and take appropriate actions to retain them. By utilizing machine learning algorithms and analyzing customer attributes, businesses can proactively develop strategies to reduce churn and improve customer retention. This repository provides a framework for Telco customer churn prediction and can be further customized and extended based on specific requirements and datasets.
