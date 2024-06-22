
# Day 4: Regression
-----------------------------------------------
## Date: 22/6/2024
### Topic:
	-Regression
	-Types of Regression
	

### Supervised Learning:
------------------- 
	-Regression
		-Labelled (Input + Output(Target attribute)
		-Task: To predict the continuous value
		
	-Classification
		-Labelled (Target attribute)
		-Task: To identify the particular class label

### Regression:
------------
	-Linear Regression:
	-LR is a type of supervised learning that computes the linear relationship between a dependent and independent features.

### Simple Linear Regression:
--------------------------
	-SLR : 1 Independent variable & 1 Dependent variable.
	
### Multiple Linear Regression:
----------------------------
	-MLR : more that 1 Independent variable & 1 Dependent variable.
	
### Steps in Regression model implementation:
------------------------------------------

	1. Importing the libraries and dataset
	2. Splitting the dataset into the Training set and Test set
	3. Preprocessing if required
	4. Fitting Simple Linear Regression to the Training set
	5. Predicting the Test set results
	6. Visualizing the Test set results
	
	
### Evaluation Metrics:
------------------
![image](https://github.com/Kiranwaghmare123/PG-DBDA-Sep2023/assets/72081819/5d14effe-cffb-4b4b-aa69-68186a40342b)

    1. Coefficient of Determination: 
    	-Also refered as R-Squared
    	-It is a statistics that indicates how much variation the developed model can capture
![image](https://github.com/Kiranwaghmare123/PG-DBDA-Sep2023/assets/72081819/4fce608b-8531-44fc-acbb-75010a7458a1)

   	
    	
    2. Residual Sum of Squares:RSS
    	-The sum of squares of the residual for each data point in the plot or data is known as RSS.
  ![image](https://github.com/Kiranwaghmare123/PG-DBDA-Sep2023/assets/72081819/59ef5a6a-30e8-4580-9ef7-b8605dfadd07)

  ![image](https://github.com/Kiranwaghmare123/PG-DBDA-Sep2023/assets/72081819/169c4933-7381-421f-81c2-4886b09d6c80)

	
    3. Total sum of squares:TSS
    	-Sum of the data points errors from the answer variables's mean is known as the total sum of squares or TSS
 ![image](https://github.com/Kiranwaghmare123/PG-DBDA-Sep2023/assets/72081819/13552cda-408a-488a-bdc9-b654767dc6f2)
   	
    4. Root Mean Squared Error:RMSE
    	-The square root of the residual variance is the RMS errors.
    	-It describe how well the observed data points match the expected values or the models absolute fit to the data.
 ![image](https://github.com/Kiranwaghmare123/PG-DBDA-Sep2023/assets/72081819/70aa2044-0255-40a3-869e-7b77f79426e8)
    
# Interview Questions

    1. What are the different types of regression.
    
    2. Is regression a supervised learning? Why?
    
    3. Explain the ordinary least squares method for regression.
    
    4. What are linear, multinomial and polynomial regressions.
    
    5. If model used for regression is
    y = a + b(x − 1)2;
        is it a multinomial regression? If not, what type of regression is it?
        
    6. What does the line of regression tell you?

# Home work
    EX 1: Loan application with loan dataset.
    
    Ex 2: Apply regression with boston dataset.
    
    Ex 3: Apply regression with tips dataset.
    
    Ex 4: Apply regression with iris dataset.  
