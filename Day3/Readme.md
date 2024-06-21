
# Day 3: Data Modelling
-----------------------------------------------
### Date: 21/6/2024
### Topic:
	-Data
	-Types of Attributes
	-Preprocessing
	-Transformations
	-Measures
	-Visualization

### ML Application Development:
---------------------------
    1. Task: Problem definition
    2. Collection of data
    3. Clean & process that data (Pre-processing)
    4. Feature Transformation
    5. Feature Selection
    6. Learning algorithm
    7. Evaluation, Visualization, and Interpretation---> (Hidden information)
    8. Conclude

### Data: a collection of data objects and their attributes
![image](https://github.com/Kiranwaghmare123/PG-DBDA-Sep2023/assets/72081819/01e81091-32ae-4aa0-b101-ea0723f849ef)

### Types of Data:
    -Numerical: Made up of numbers
    	-Continuous: infinite real numbers
    	-Discrete: finite
    	
    -Categorical: Made up of words
    	-Ordinal: Distinct & ordered
    		Eg: eye color, zip codes
    	
    	-Nominal:Distinct
    		Eg: Ranking list
    		
    	-Interval: Range
    		Eg: Temperature
    		
    	-Ratio: All
    		Eg: Girls-Boys ratio
    	
    	Ex: Age: 15 to 78yrs
    		-<20yrs : Teen
    		-20 to 45yrs : Yng
    		->40yrs : Adult

### Types of dataset:
-----------------
  	-Record
  		-Data Matrix
  		-Document data
  		-Transaction data
  	-Graph
  		-World Wide Web
  		-Molecular data structure
  	-Ordered
  		-Spatial data
  		-Temporal(time series) data
  		-Sequential data
  		-Genetic data
  		
### Knowledge Discovery Process:
-------------------------------
    1. Goal:
    	-understanding the application domain and goals of the KDD effort
    2. Data selection, acquisition, integration
    3. Data cleaning
    	-noise, missing data, outliers, etc.
    4. Exploratory data analysis
    	-Dimensionality reduction, transformation
    	-selection of an appropriate model for analysis, hypothesis testing
    5. Data mining/Machine Learning
    	-selecting appropriate methods that match set goals ( classification, regression, clustering)
    6. Testing and verification
    7. Interpretation
    8. Conclusions
![image](https://github.com/Kiranwaghmare123/PG-DBDA-Sep2023/assets/72081819/021b520a-e93d-49f8-9ef5-28a3b8550dd3)

### Data Pre-processing steps:
----------------------
    1. Get the dataset
    2. Import libraries
    3. Import dataset
    4. Analyse the data & identify the missing data
    5. Apply feature transformation
    6. Split the dataset into training and testing data
    
 ![image](https://github.com/Kiranwaghmare123/PG-DBDA-Sep2023/assets/72081819/72158265-ee60-45f9-adec-6ed66fbcb2f6)
   
    
### Feature Transformation:
-----------------------------
  #### Label Encoding:
     Label encoding is a technique used in machine learning and data analysis to convert categorical variables into numerical format. It is particularly useful when working with algorithms that require numerical input, as most machine learning models can only operate on numerical data.
![image](https://github.com/Kiranwaghmare123/PG-DBDA-Sep2023/assets/72081819/b838612d-c0ce-434e-9815-1309906d7d49)

  #### Onehot Encoding: 
    One Hot Encoding is a technique that is used to convert categorical variables into numerical format.
![image](https://github.com/Kiranwaghmare123/PG-DBDA-Sep2023/assets/72081819/060dd00c-094f-4039-a9eb-d7924fd0b711)

### Feature Scaling:
-----------------
![image](https://github.com/Kiranwaghmare123/PG-DBDA-Sep2023/assets/72081819/c8de4131-de9e-411d-8343-c43ace77a644)

![image](https://github.com/Kiranwaghmare123/PG-DBDA-Sep2023/assets/72081819/d40feda0-01af-4713-9d15-d7e01a173524)

# Homework:
------------

# Ex 1:
    data = {
        'age': [25, np.nan, 35, 45, 55, 65, 75, 85, 95, 105],
        'salary': [50000, 60000, np.nan, 80000, 90000, 100000, 110000, 120000, np.nan, 140000],
        'gender': ['Male', 'Female', np.nan, 'Female', 'Male', 'Female', 'Male', 'Male', 'Female', 'Male'],
        'purchased': ['No', 'Yes', 'No', 'No', 'Yes', 'Yes', 'No', 'Yes', 'No', 'Yes']
    }

# Ex 2:
    data = {
        'age': [23, 30, np.nan, 45, 56, 67, np.nan, 89, 34, 29, 50, 70, 22, 38, 60],
        'income': [48000, 52000, 58000, np.nan, 70000, 89000, 92000, 130000, np.nan, 46000, 78000, 85000, 40000, 65000, np.nan],
        'gender': ['Female', 'Male', 'Female', np.nan, 'Male', 'Female', 'Female', 'Male', 'Female', 'Male', np.nan, 'Male', 'Female', 'Male', 'Female'],
        'city': ['New York', 'Los Angeles', 'New York', 'Chicago', 'Los Angeles', 'Chicago', 'Chicago', 'New York', 'Los Angeles', 'Chicago', 'New York', 'Los Angeles', 'Chicago', 'Los Angeles', 'New York'],
        'bought': ['Yes', 'No', 'Yes', 'No', 'Yes', 'No', 'No', 'Yes', 'Yes', 'No', 'Yes', 'No', 'Yes', 'No', 'Yes']
    }

# Ex 3:
    data = {
    'age': [25, 30, 35, np.nan, 45, 50, 55, 60, np.nan, 70, 75, 80, 85, 90, np.nan],
    'height_cm': [170, 165, 180, 175, np.nan, 160, 155, 150, 165, np.nan, 175, 180, 170, 160, 155],
    'weight_kg': [65, 70, 75, 80, 85, np.nan, 95, 100, 105, 110, 115, np.nan, 85, 70, 65],
    'gender': ['Male', 'Female', np.nan, 'Female', 'Male', 'Female', 'Male', np.nan, 'Female', 'Male', 'Female', 'Male', 'Female', np.nan, 'Female'],
    'activity_level': ['High', 'Medium', 'Low', 'Medium', 'High', 'Low', np.nan, 'High', 'Medium', 'Low', 'Medium', 'High', 'Low', 'Medium', np.nan],
    'diet': ['Vegetarian', 'Non-Vegetarian', 'Vegan', 'Vegetarian', np.nan, 'Non-Vegetarian', 'Vegan', 'Vegetarian', 'Non-Vegetarian', 'Vegan', np.nan, 'Vegetarian', 'Non-Vegetarian', 'Vegan', 'Vegetarian'],
    'target': ['Yes', 'No', 'Yes', 'No', 'Yes', 'No', 'Yes', 'No', 'Yes', 'No', 'Yes', 'No', 'Yes', 'No', 'Yes']
}

# Ex 4:

    Ex: data = {
    'client_id': [46109, 46109, 46109],
    'loan_type': ['home', 'credit', 'home'],
    'loan_amount': [13672, 9794, 12734],
    'repaid': [0, 0, 1],
    'loan_id': [10243, 10984, 10990],
    'loan_start': ['2002-04-16', '2003-10-21', '2006-02-01'],
    'loan_end': ['2003-12-20', '2005-07-17', '2007-07-05'],
    'rate': [2.15, 1.25, 0.68]
    }
