# End to End Machine Learning Project

# Student Performance Indicator - Vinay Kiran Reddy
## Life cycle of Machine learning Project
* Understanding the Problem Statement
* Data Collection
* Data Checks to perform
* Exploratory data analysis
* Data Pre-Processing
* Model Training
* Choose best model

## 1) Problem statement
This project understands how the student's performance (math scores) is affected by other variables such as Gender, Ethnicity, Parental level of education, Lunch and Test preparation course.

## 2) Data Collection
Dataset Source - https://www.kaggle.com/datasets/spscientist/students-performance-in-exams?datasetId=74977
The data consists of 8 column and 1000 rows.

### Dataset Information

There are 7 independent variables:

* gender : sex of students -> (Male/female)
* race/ethnicity : ethnicity of students -> (Group A, B,C, D,E)
* parental level of education : parents' final education ->(bachelor's degree,some college,master's degree,associate's degree,high school)
* lunch : having lunch before test (standard or free/reduced)
* test preparation course : complete or not complete before test
* reading score
* writing score

Target variable:
* math score

# Student Performance Indicator Website Link :

[Website](http://127.0.0.1:5000/predictdata)

# AWS Deployment Link :

AWS Elastic Beanstalk link : [http://gemstonepriceutkarshgaikwad-env.eba-7zp3wapg.ap-south-1.elasticbeanstalk.com/](http://gemstonepriceutkarshgaikwad-env.eba-7zp3wapg.ap-south-1.elasticbeanstalk.com/)

# Screenshot of UI

![HomepageUI](./Screenshots/HomepageUI.jpg)


# Approach for the project 

1. Data Ingestion : 
    * In Data Ingestion phase the data is first read as csv. 
    * Then the data is split into training and testing and saved as csv file.

2. Data Transformation : 
    * In this phase a ColumnTransformer Pipeline is created.
    * For Numeric Variables first SimpleImputer is applied with strategy median , then Standard Scaling is performed on numeric data.
    * For Categorical Variables SimpleImputer is applied with most frequent strategy, then one hot encoding is performed , and finally, the data is scaled with Standard Scaler.
    * This preprocessor is saved as pickle file.

3. Model Training : 
    * In this phase base model is tested . The best model found was Linear Regression.
    * After this hyperparameter tuning is performed.
    * This model is saved as pickle file.

4. Prediction Pipeline : 
    * This pipeline converts given data into dataframe and has various functions to load pickle files and predict the final results in python.

5. Flask App creation : 
    * Flask app is created with User Interface to predict the student math_score inside a Web Application.

# Exploratory Data Analysis Notebook

Link : [EDA Notebook](./notebook/notebook/1_EDA_STUDENT_PERFORMANCE.ipynb)

# Model Training Approach Notebook

Link : [Model Training Notebook](./notebook/notebook/notebook/2_MODEL_TRAINING.ipynb)

