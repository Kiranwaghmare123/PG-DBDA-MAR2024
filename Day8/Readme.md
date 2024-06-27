# Day 8: Naive Bayes & KNN
-----------------------------------------------
## Date: 27/06/2024


Parametric and Nn-Parametric Methods:
--------------------------------------

	Parametric Methods:
	--------------------
	-Parametric method rely on specific assumptions about the population distribution,
	-assume that data follws a known probabiltiy distribution, such as normal or gaussian distribution.
	-Fixed parameters: use to set of fixed parameters to determine a probabiltiy model.
	
	Assumptions: 
	------------
	-Data follows a normal distribution.
	-Independence: Data setobservation are independent.
	-Homogeneity of variance: Variance is consistent across the group.
	
	Statiscal Test:
	---------------
	-t-test
	-ANOVA
	-F-test
	-Chi-square test
	-Correlation analysis
	
	Algorithms involved:
	-----------------------
	-Linear Regression
	-Logistic REgression
	-Naive Bayes

Non-parametric Methods:
------------------------
	-Non-parametric methods do not rely on specific distribution assumption. 
	-distribution-free
	-No fixed parameter
	
	Statistical Tests:
	--------------------
	-Mann-Whitney U test:Difference between the medians of 2 groups
	-Kruskal-Wallis test:Difference between the medians of 3 or more groups
	
	
	Algorithms involved:
	--------------------
	-K-Nearest Neighbour ( K-NN)
	-Decision tree
	-Support Vector Machine
	-Neural Networks
	
Naive Bayes:
------------
	-Collection of classification algorithm based on Bayes Theorem
	-not a single algorithm but a family algorithm where all of them share a common principle of pprobability calculation.
	-Every pair of feature being classified is independent of each other.

![image](https://github.com/Kiranwaghmare123/PG-DBDA-MAR2024/assets/72081819/5e680ed6-e6b0-4912-a24b-1a81bfc7d7f8)

-Bayes Theorem:
--------------
	-This theorem calculates the probability of an event occuring given by the probability of another event(feature independence).

	p(A/B) = [P(B/A).P(A)]/P(B)

	-P(A): prior probability
	-P(B):Marginal probability
	-P(A/B):Posterior probability of A given B/A
	-P(B/A):Likelihood of B given A
![image](https://github.com/Kiranwaghmare123/PG-DBDA-MAR2024/assets/72081819/6c748b82-78e8-470a-b698-c9bd3f6ecd9b)
	
	-Naive : name indicates the simplifying asumptions made by the Naive Bayes classifier.
	-classifier assumes that the feature used to describe an observation are conditionally independent, for given class label.

Types of Naive Bayes Model:
----------------------------
	1. Gaussian Naive Bayes Classier:
	![image](https://github.com/Kiranwaghmare123/PG-DBDA-MAR2024/assets/72081819/5ae1a805-5005-4d84-8606-509a00e7c798)

	2.Bernoulli Naive Bayes Classifier:
	![image](https://github.com/Kiranwaghmare123/PG-DBDA-MAR2024/assets/72081819/b8c69b64-862a-4b8b-bf5a-abc07b0444be)

	3.Multinominal Naive Bayes Classifier
 	![image](https://github.com/Kiranwaghmare123/PG-DBDA-MAR2024/assets/72081819/f4ab828b-e6cc-4cf8-82af-d3d384581e78)


#Reference: Tutorial for Naive Bayes
	Link : https://aihubprojects.com/naive-bayes-algorithm-from-scratch/

Cross validation:
------------------
	-cross validation is a technique used to evaluate the performance of a model on unseen data.	
	-Purpose:prevents overfitting by providing a realistic estimate of model performance on new data.


Types of Cross-validation:
--------------------------
	1.Holdout validation:
		-Training on 50% and Testing on 50%
		-simple and quick technique
		-High bias: due to less data.
		
	2. Leave One Out Cross Validation(LOOCV):
		-Taining on n-1 records and Testing on 1 sample records
		-Low bias:uses all data points for training
		
	3.Stratified Cross Validation:
		-Maintain class distribution in each fold,specially used for imbalanced dataset.
		
	4.K-Fold Cross Validation:
		-Dataset is split into k subsets(folds), each fold used for testing once.
		-Iterates k times, each iteration with a different testing fold dataset.
		-Most common value for k: k=10 for a good balance of bias and variance.
  
	![image](https://github.com/Kiranwaghmare123/PG-DBDA-MAR2024/assets/72081819/84bd1d84-dd58-4989-8f9a-b1c2dd53557c)
	
		
K-Nearest Neighbour (K-NN) Algorithm:
--------------------------------------
	-supervised learning technique used for both classification and regression.
	
	-non-parametric algorithm, meaning it does not make any assumption about underlying data distribution.
	
	-It classifies or predicts the value of new data points based on the majority vote(for classification) and average (for regression) of its nearest neighbour.
	
	-basic idea: to classify a data point based on how it's neighbour are classified.

Use of K-NN:
------------
	-Simplicity:Easy to implement and understand.
	-Non-parametric:No assumptions for the data distributions
	-Handles numeric and categorical dataset.
	-Less sensitive compared to other algorithms.(Robust to outliers)
	![image](https://github.com/Kiranwaghmare123/PG-DBDA-MAR2024/assets/72081819/aea4775c-c1b5-4b8b-aa27-7d81f7de82d2)

# Distance Measure
![image](https://github.com/Kiranwaghmare123/PG-DBDA-MAR2024/assets/72081819/d10b8eb0-9ce2-4479-b534-81bcad24c3a1)


Curse of Dimensionality:
-------------------------
	-A phenomenon where the accuracy and effectiveness of algorithms deteriores as the dimensionality of the data increses exponentially.
	
	-Dimension:Features or attributes od data

Challenges:
----------
	-Data points becomes sparse in high dimensional space.
	-Difficulty in identification of meaningful patterns in our data.
	-Increase computational complexity and resource requirements.
	-Higher risk of overfitting and correlations.

Solution:
----------
	1.Dimension Reduction Techniques:
	
	-Feature Seletion:
		-Identify and select relevant features.
		-Discard the irrelavant or redundant features.
		
	-Feature Extraction:
		-Transform high dimensional data into a lower dimensional data
		-Techniques: PCA (Principal Componenet analysis)
	
	
2.Data Preprocessing:
	
	-Normalization:
			-Scale feature to a similar range.
			
	-Handle Missing values:
			-Address missing data through imputation or deletion.
		
Principal Componenet Analysis:
------------------------------
	-PCA is a dimensionality reduction technique.
	-It reduces the dimensionality of a dataset while preserving as much as variance.
	-Converts correlated variables into a set of uncorrelated variables, called as principal components (PC)
	-It is widely used in EDA analysis and for feature selection.

Steps:
------
	1. Standardization:
		-Normalize the data so each feature has mean 0 and std dev of 1.
	
	2. Covariance Matrix Computation
		-Compute the covariance matrix tounderstand the relationship between variables.
		
	3. Compute Eigenvalues and Eigen vectors:
		-Identify the principal componenet using eigen vector and eigenvalues.
		
	4. Sort Eigenvalues and Eigenvectors:
		-Detemines the amount of variance of each principal component.
	
	5. Select the Principal components
		-Choose the components that meet a predefined threshold of explained variance.
		
	6.Project Data onto Principal Componenets:
			-Transform the data to the new feature space using principal component
		
	

# Visualising the Training data code for today's application


# Accuracy Rate:

    accuracy_rate = []
    for i in range(1,40):
        
        knn = KNeighborsClassifier(n_neighbors=i)
        score=cross_val_score(knn,df_feat,df['TARGET CLASS'],cv=10)
        accuracy_rate.append(score.mean())

# Error Rate:
        error_rate = []
        
        for i in range(1,40):
            knn = KNeighborsClassifier(n_neighbors=i)
            score=cross_val_score(knn,df_feat,df['TARGET CLASS'],cv=10)
            error_rate.append(1-score.mean())

        error_rate = []
        
        # Will take some time
        for i in range(1,40):
            
            knn = KNeighborsClassifier(n_neighbors=i)
            knn.fit(X_train,y_train)
            pred_i = knn.predict(X_test)
            error_rate.append(np.mean(pred_i != y_test))
        plt.figure(figsize=(10,6))
        #plt.plot(range(1,40),error_rate,color='blue', linestyle='dashed', marker='o',
          #       markerfacecolor='red', markersize=10)
        plt.plot(range(1,40),accuracy_rate,color='blue', linestyle='dashed', marker='o',
                 markerfacecolor='red', markersize=10)
        plt.title('Error Rate vs. K Value')
        plt.xlabel('K')
        plt.ylabel('Error Rate')

# Ex 1:
    weather=['Sunny','Sunny','Overcast','Rainy','Rainy','Rainy','Overcast','Sunny','Sunny',
    'Rainy','Sunny','Overcast','Overcast','Rainy']
    temp=['Hot','Hot','Hot','Mild','Cool','Cool','Cool','Mild','Cool','Mild','Mild','Mild','Hot','Mild']
    
    play=['No','No','Yes','Yes','Yes','No','Yes','No','Yes','Yes','Yes','Yes','Yes','No']
