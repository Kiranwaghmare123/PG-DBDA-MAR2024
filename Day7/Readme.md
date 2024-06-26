# Decision Tree:
--------------
    -A flowchart like structure used for decision making or predictions.
    -It consist of nodes(decision nodes), branches(outcome) and the leaf nodes(predictions).
    -Internal node: attributes
    -Branches: sub attributes in the feature column
-Leaf nodes: Final class labels

# Working of Decision tree:
    --------------------------
    1.Selecting the best attribute: 
    	-use metric like Gini impurity, entropy or information gain.
    2.Splittng of the dataset:
    	-Split into subsets based on the slected attribute.
    3.Repeatation of the process:
    	-Recursively repeat for eacj subset until a stopping criteria is met.
	
# Metrics for Splitting:
----------------------
    1. Entropy : Amount of uncertainity or impurity
    Formula:
    
    where, pi is the probability of an instance being classified into a particular class.
    
    
    2. Information Gain : Reduction in entropy or gini impurity.
    Formula:
    
    Information Gain = Entropy(parent) - Average Entropy of Feature column
    
    
    3.Gini impurity: Likelihood of incorrect classification
    Formula:
    
    where, pi is the probability of an instance being classified into a particular class.
    
    
# Advantages:
-----------
    -Easy to understand and interpreat.
    -Suitable for classification and regression.
    -No need for feature scaling.
    -Handles non-linear relationships effectively.

# Disadvantages:
---------------
    -Overfitting : prone to overfitting, especially with deep trees.
    -Instability: Sensitive to small variations in the data.
    -Bias towards features with more leveles.

# Pruning:
---------
    -method to help overfitting.
    -helps in improving the performance of the tree by cutting the nodes which are not significant.
    -2 types of pruning:
    	-Pre-pruning: (Early stopping): Stops tree growth based on criteria
    		-e.g. max depth, min samples leaf.
    	
    	-Post-pruning: Removes branches from a fully grown tree that offer little classification power.

# Decision Tree Regression:
--------------------------
    -Decision tree regression is used for predictive modelling.
    -operated by recursively partitioning the dataset into subsets nased on the input features.
    -create a hierarchical tree-like structure with internal nodes for decisions and leaf nodes for predicted output.
    -aim to minimize variance in the target variable within each partition.

# Advantages:
-------------
    -Easy to understand and visualize decision tree rules.
    -Capture non-linear relationships.
    -No feature scaling is required.
    -Handles numerical and categorical data
    -Outliers have minimal impact on overall model performance.

# Random Forest:
---------------
    -It is a supervised learning used for both classification and regression task.
    -Concept: It consist of collection of decision tree that operates on various subsets of the dataset. The final output is determined by aggregating the prediction of these trees, which is typically called as majority voting.

# Assumptions:
------------
    -The feature values should contain actual values for accurate predictions.
    -The predictions from each tree should have low correlation to ensure diverse and accurate results.

# Importance of Random Forest:
----------------------------
    -Overfitting prevention
    -Accuracy
    -Efficient 

# Working of Random Forest:
-------------------------
    1.Select Random data points from the training dataset.
    2.Build Decision Tree
    3.Choose the number of tree to build (n_estimator = n)
    4.Make predictions


# Data Preparing for Random Forest Model:
---------------------------------------
    -Handle the missing values
    -Addressing the imbalance data is required.


# Ensemble Learning:
------------------
    -Ensemble learning is a machine learning program where multiple models, often called "weak learners" are trained to solve the same problem and combined to get better results.
    -Main Idea : to use a group of diverse models to achieve better performance than any single model.
    

# Types of Emsemble learning:
---------------------------
  1. Bagging
  2. Boosting
  3. Random space
  4. Stacking




# Home work:
# EX1: Identify the root node for the decision tree using following dataset.
  ![image](https://github.com/Kiranwaghmare123/PG-DBDA-MAR2024/assets/72081819/c45b7035-e2c4-44ac-9528-0827c63644bf)

# Ex 2: Implement Decision Tree using iris dataset.
