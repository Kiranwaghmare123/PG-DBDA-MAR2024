# Day 2: Libraries in Machine Learning
=================================================
### Date: 20/06/2024
### Topics:
------------------
	
	-Introduction to ML Libraries
	-Numpy
	-Pandas
	-Matplotlib
	-Seaborn
	-ML Model
	-ML features and importance
	-Steps to start ML
	-ML Lifecycle
	-ML Challenges 
	
### ML Model:
----------
	- Machine Learning is a concept that allows the machine to learn from examples and experience, and that too without being explicitly programmed.
	
	-Data: split it into the Training and Testing phase

### Steps in Machine Learning Model

	
	1.	Define the Problem:
	2.	Collect Data:
	3.	Explore the Data:	
	4.	Pre-process the Data:		
	5.	Split the Data:		
	6.	Choose a Model:
	7.	Train the Model:	
	8.	Evaluate the Model:	
	9.	Fine-tune the Model:		
	10.	Deploy the Model:		
	11.	Monitor the Model:
 
### ML Lifecycle:
	
	1.	Study the Problem:
	•		Understand the business problem and define the objectives of the model.
	2.	Data Collection:
		•	Collect relevant data required for the model.
		•	Data sources include databases, APIs, and web scraping.
	3.	Data Preparation:
		•	Check and format the data to make it suitable for modeling.
		•	Steps involved:
			•	Data cleaning
			•	Data transformation
			•	Exploratory data analysis and feature engineering
			•	Split the dataset into training and testing sets
	4.	Model Selection:
		•	Choose the appropriate machine learning algorithm suitable for the problem.
		•	Sometimes, multiple models are used and compared to select the best one based on requirements.
	5.	Model Building and Training:
		•	Build the model after selecting the algorithm.
		•	For traditional machine learning:
			•	Involves tuning a few hyperparameters.
		•	For deep learning:
			•	Define layer-wise architecture, input and output size, number of nodes in each layer, loss function, gradient descent optimizer, etc.
		•	Train the model using the preprocessed dataset.
	6.	Model Evaluation:
		•	Evaluate the trained model on the test dataset to determine its accuracy and performance.
		•	Techniques used:
			•	Classification report
			•	F1 score
			•	Precision
			•	Recall
			•	ROC curve
			•	Mean squared error
			•	Absolute error
	7.	Model Tuning:
		•	Based on evaluation results, tune or optimize the model to improve performance.
		•	Involves tweaking the hyperparameters of the model.
	8.	Deployment:
		•	Deploy the trained and tuned model in a production environment.
		•	Integrate the model into an existing software system or create a new system for the model.
	9.	Monitoring and Maintenance:
		•	Continuously monitor the model’s performance in the production environment.
		•	Perform maintenance tasks as required.
		•	Monitor for data drift, retrain the model as needed, and update the model as new data becomes available.
	
# Home-Work
### Homework Assignment : Exploratory Data Analysis (EDA) with the Iris Dataset

	The Iris dataset is a classic dataset for data analysis and machine learning. It includes 150 observations of iris flowers with four features: sepal length, sepal width, petal length, and petal width, along with the species of the flower.
	
	**Assignment Questions:**

	1. Load the Iris dataset and display the first few rows.
	2. Display summary statistics of the dataset.
	3. Create histograms for each feature.
	4. Create box plots to show the distribution of each feature.
	5. Create scatter plots to show relationships between pairs of features.
	6. Create a pair plot to visualize the relationships between all features.
	7. Create a correlation matrix heatmap.

# Sample dataset
 Ex 1:
	data = {
    'Name': ['Alice', 'Bob', 'Charlie', 'David'],
    'Age': [24, 27, 22, 32],
    'City': ['New York', 'Los Angeles', 'Chicago', 'Houston']
}

	Ex 2:
	data = [
    {'Name': 'Alice', 'Age': 24, 'City': 'New York'},
    {'Name': 'Bob', 'Age': 27, 'City': 'Los Angeles'},
    {'Name': 'Charlie', 'Age': 22, 'City': 'Chicago'},
    {'Name': 'David', 'Age': 32, 'City': 'Houston'}
]

	Ex3:
	df1 = pd.DataFrame({
    'A': ['A0', 'A1', 'A2', 'A3'],
    'B': ['B0', 'B1', 'B2', 'B3'],
    'key': ['K0', 'K1', 'K2', 'K3']
})

df2 = pd.DataFrame({
    'C': ['C0', 'C1', 'C2', 'C3'],
    'D': ['D0', 'D1', 'D2', 'D3'],
    'key': ['K0', 'K1', 'K2', 'K3']
})

	Ex 4:
	df1 = pd.DataFrame({
		'A': ['A0', 'A1', 'A2'],
		'B': ['B0', 'B1', 'B2']
	}, index=['K0', 'K1', 'K2'])

	df2 = pd.DataFrame({
		'C': ['C0', 'C1', 'C2'],
		'D': ['D0', 'D1', 'D2']
	}, index=['K0', 'K2', 'K3'])
	
	Ex 5:
	df = pd.DataFrame({
    'Category': ['A', 'A', 'B', 'B', 'C'],
    'Values': [1, 2, 3, 4, 5]
	
	
# Interview Questions:
	1. Explain the need for Machine Learning.
	2. Explain the challenges or limitations of Machine Learning
	3. Explain why Machine Learning is so popular.
	4. Explain the different types of Data Analysis.
 	5. Explain the different applications in machine learning.
