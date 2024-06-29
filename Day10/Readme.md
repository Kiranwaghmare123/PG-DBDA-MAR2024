# Day 11: Unsupervised Learning
-----------------------------------------------
## Date: 29/06/2024
## Topic:
	-Clustring Algorithms
	-K-Means
	-Agglomerative
	-Divisive
	-DBSCAN
### Unsupervised Learning:
-----------------------
    -In Machine learning 2 main types of learning:
    	-Supervised
    	-Unsupervised

    -Unsupervised: Machine learns from unlabelled data(input data without explicit output.)
    -Objective: discover patterns and relationships in the data.
    
### -Techniques:
	-Clustering
	-Dimension reduction
	-Anomaly detection
	
### Types of unsupervised learning:
-------------------------------
    1. Clustering:
    	-Groups of similar data points.
    	
    2. Association Rule Mining (Market Basket analysis):
    	-Identifies patterns and relationships among the different products.
    	
    
    ### Clustering :
-------------
	-unsupervised learning method
	-used to draw references from datasets consisting of input data without labeled responses.
	-used to find meaningful structures, expalnatory process, generative features, and grouping inherent elements in a set of examples.
	
### Cluster:
--------
	-a collection of data objects.
	-similar to one another within the same cluster.
	-dissimilar to the objects in the cluster.
	
### Cluster analysis:
-----------------
	-a process of finding similarities between data according to the characteristics found in the data and grouping similar data objects into clusters.
	
### Applications in Clustering:
----------------------------
	-Standalone tool: to get insight into data distribution.
	-Pattern analysis/ Pattern Recognition
	-Spatioal Data Analysis
	-Imge Processing

### Good cluster:
-------------
	-A good clustering method will generate high quality clusters with
		-Inter-class similarity
		-Intra-class similarity
	-quality of a cluster results depends on both the similarity measures used by the method and it's implementation.
	-quality of a clustering method is also measured by itsability to discover the hidden pattens in the dataset.
	

### Clustering Measures:
---------------------
	1. Data Matrix
	2. Distance Matrix
		-Jaccard similarity (Binary values)
		-Other distance measues:
			1. Minkowski distance
			2. Manhattan distance
			3. Euclidean distance
			4. Weighted distance
			
### Clustering Techniques:
----------------------
	1. Partitioning Clustering
	2. Hierarchical Clustering
	3. Density based Clustering
	4. Graph method Clustering
	5. Model based Clustering
	
### 1. Partitioning Clustering :
-----------------------------
	-partition the object into k-clusters and each partition forms one cluster.
	-used to optimize an objective criteria similarity function such as when the distance is a major parameter.
	-Eg: K-Means, K-Medoid
	
### 2. Hierarchical Clustering :
-----------------------------
	-Clusters are formed a tree-like structure based on the hierarchy.
	-2 types of tree constructions:
		-Agglomerative ( Bottom-up approach)
		-Divisive ( Top-Down approach)
		
### 3. Density based Clustering :
-----------------------------
	-method where cluster are in dense region having some similarities and differences from the lower dense region of the space.
	-methods works with good accuracy and the ability to merge 2 clusters.
	-Eg: DB-SCAN algorithm.
	
### 4. Graph method Clustering :
-------------------------------
	-data space is formulated into a finite number of cells that form a grid like structure
	-Clustering operations can be done on these grids.
	-Eg: STING algorithm


### 5. Model based Clustering :
---------------------------
	- a model is hypothesized for each of the cluster and tries to find the best fit of thet model.
	
### K-Means Algorithm:
------------------
	-process of partioning method that divides a dataset into 'k' distint clusters based on similarity aiming to minimize the variance within each cluster.
	-Problem of Kmeans: 
		-K-Means is very sensitive to outliers.
	-Solution: 
		-K-Medoid (work on the principle of median values)

 
### Advantages:
------------
    -No need of labelled data.
    -Effective for dimensionality reduction
    -Uncovers hidden patterns
    -provides insight from unlabeled data


### Disadvantages:
--------------
    -Difficult to measure accuracy without predefined labels.
    -Requires interpretation and labeling by the user.
    -Sensitive to data quality, missing values, outliers and noise.


### K-Means:
--------
    It is a popular unsupervised ML algorithm used to partition a dataset into k distinct cluster.
    
    Working of K-MEans:
    -------------------
    1. Inialization: 
    	-slect k intial centroid randomly from the dataset.
    2. Assignment: 
    	-Assign each data point to the nearest centroid forming k clustes.
    3. Update:
    	-Recompute the centroid as the mean of all data points assigned to each other.
    4.Repeat:
    	-Repeat the assignment and update steps until the centroids do not change significantly, or a maxmum number of iterations is reached.
    

# Visualize the cluster
    plt.scatter(X[y_kmeans == 0, 0], X[y_kmeans == 0, 1], s = 100, c = 'red', label = 'Cluster 1')
    plt.scatter(X[y_kmeans == 1, 0], X[y_kmeans == 1, 1], s = 100, c = 'blue', label = 'Cluster 2')
    plt.scatter(X[y_kmeans == 2, 0], X[y_kmeans == 2, 1], s = 100, c = 'green', label = 'Cluster 3')
    plt.scatter(X[y_kmeans == 3, 0], X[y_kmeans == 3, 1], s = 100, c = 'cyan', label = 'Cluster 4')
    plt.scatter(X[y_kmeans == 4, 0], X[y_kmeans == 4, 1], s = 100, c = 'magenta', label = 'Cluster 5')
    plt.scatter(kmeans.cluster_centers_[:, 0], kmeans.cluster_centers_[:, 1], s = 300, c = 'yellow', label = 'Centroids')
    plt.title('Clusters of customers')
    plt.xlabel('Annual Income (k$)')
    plt.ylabel('Spending Score (1-100)')
    plt.legend()
    plt.show()
