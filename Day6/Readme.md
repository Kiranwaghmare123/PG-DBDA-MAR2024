
# Day 5: Regression
-----------------------------------------------
# Date: 25/06/2024
# Topic:
	-Regression Analysis
	-Types of Regression
		-Simple Linear Regression
		-Multiple Linear Regression
		-Polynomial Linear Regression
		-Ridge Regression
		-Lasso Regression
		-Elastic Net Regression
	-Logistic Regression
	
# Regression Analysis:
 -------------------
     -statistical analysis method to model the relationship between IV(X) (one  or more) and  DV(Y)
     -understand how the DV changes as per the changes in IV-Key feature: helps to find coorelation between variable to predict continuous outcomes.
     -Applications: Prediction, forcasting , time series, cause -effect relationship
     -Terminologies:
    	 -IV
    	 -DV
    	 -Multicolliniarity: high correlation among IV.
    	 -Underfitting:Poor model performance on training dataset
    	 -Overfitting:Model performs well on training dataset but poorly perform on testing dataset.
	 
# Types of Regression:
---------------------
    1.SLR
    2.MLR
    3.Polynomial REgression

# Model performance:
------------------
    Best fit Line: Determine how well the regression line fits the observation.
    -R-square 
    	-Measure the strength of the relationhip between dependent and independent variable,
    	-0-100% (0-1), higher values indicates better model fit.
    	-also called it as the coefficient of determination.
	
	
# Assumptions of Linear REgression:
--------------------------------
    -Linear Relationship:
    -No multicolliniarity
    -No Homoscedacity: Assumes that the error term is the same  for all the values of the independent variable.
    -Normal distributed of error terms
    -No Autocorrelation:Asuumes no correlation in error terms.It will reduce model accuracy.
	
# Overfitting:
------------
	-phenomenon that occurs when a machine learning model is conatrained to the training set and not able to perform well on unseen data.
	-when model learns the noise in the training data as well, cases will be remembered by the training data set.
	-Result: Training accuracy increase, Testing accuracy decreases.
	

# Underfitting:
------------- 
	-phenomenon that occurs when a machine learning model is notable to learn even the basic patterns available in the dataset.
	-such model is unable to perform well even ontraining dataset.
	-Result: Training and Testing accuracy decreases.
	
	
# Bias:
----- 
	-refers to the error which occurs when we try to fit perfectly.
	-data fit will be high bias, where is unable to learn the patterns in the data and hence perform poorly.
	
# Variance:
---------
	-refers to the error which occurs when we try to make predictions using the unseen data.
	-data fit with high variance, where model learn noise that present in the data.

#Cheatsheet
![image](https://github.com/Kiranwaghmare123/PG-DBDA-MAR2024/assets/72081819/19ededea-22ed-446d-93d2-eae8aa7e1f2a)

# Regularization:
---------------
	- technique used to reduce errors by fitting the function appropriately on the given training set & avoiding overfitting.

# Interview Questions
---------------------
    1. What are the different types of regression.
    2. Is regression a supervised learning? Why?
    3. Explain the ordinary least squares method for regression.
    4. What are linear, multinomial, and polynomial regressions.
    5. If model used for regression is y = a + b(x − 1)2; is it a multinomial regression? If not, what type of regression is it?
    6. What does the line of regression tell you?

# Problem statement:
----------------------
### Machine Learning Problem Statement: Iris Flower Species Prediction using Linear Regression

    ### Objective:
        Develop a machine learning model to analyze the Iris dataset and predict the species of iris flowers based on various features. The model should utilize linear regression and explore the suitability of different types of regression for this classification task.

    ### Dataset:
        The Iris dataset consists of measurements for three species of iris flowers (setosa, versicolor, and virginica). The features include sepal length, sepal width, petal length, and petal width.
    
    ## Tasks:
    
    ### Data Exploration:
    
        Explore the dataset to understand the distribution of features.
        Visualize the relationships between different features.
  
    ## Data Preprocessing:
    
        Check for missing values and outliers.
        Ensure that the data is suitable for linear regression (numeric features, linear relationships).
    
    ## Feature Selection:
    
        Choose relevant features for predicting iris species.
        Consider feature scaling if necessary.

    # Linear Regression:
    
        Implement a linear regression model to predict the iris species based on the chosen features.
        Evaluate the model's performance using appropriate metrics (e.g., mean squared error).
        
    # Type of Regression:
    
        Explore different types of regression models to compare their performance with linear regression.
        Select the most suitable regression model for the Iris species prediction task.
        
    ###  Hyperparameter Tuning:
    
        Optimize hyperparameters for the selected regression model to improve performance.
    
    ### Evaluation Metrics:
    
        Utilize appropriate metrics for evaluating regression models, considering the nature of the task.
        
    ### Result Analysis:
    
        Analyze the model's predictions to understand how well it generalizes to new data.
        Interpret the coefficients and their significance in the linear regression model.
    
    ### Visualization (Optional):
    
        Optionally, visualize the regression line and scatter plots to better understand the relationships between features and species.
    
    ### Deployment (Optional):
    
        If applicable, deploy the trained regression model for making predictions on new data.

    ### Monitoring and Updating (Optional):
    
        If deployed, establish a system for monitoring the model's performance over time.
        Plan for model updates or retraining based on new data.
