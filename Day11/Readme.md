#### DBSCAN Algorithm
    - **Non-Spherical Clusters**: Effective for clusters of arbitrary shapes.
    - **Noise Handling**: Robust against noise and outliers.
    - **Limitations of Other Methods**: Partitioning (e.g., K-Means) and hierarchical clustering struggle with non-convex shapes and noise.

#### Key Parameters
![image](https://github.com/Kiranwaghmare123/PG-DBDA-MAR2024/assets/72081819/bb9fcabc-59ca-4e66-af6c-a1041666da7b)

    1. **eps (Epsilon)**:
       - Defines the radius of the neighborhood around a point.
       - Too small: Many outliers.
       - Too large: Merged clusters.
       - Determination: Use the k-distance graph.
    
    2. **MinPts (Minimum Points)**:
       - Minimum number of points within the eps radius.
       - Larger datasets require larger MinPts.
       - General Rule: MinPts ≥ D + 1 (D = number of dimensions).
       - Minimum value: At least 3.

#### Types of Data Points in DBSCAN
    1. **Core Point**: Has at least MinPts points within eps.
    2. **Border Point**: Has fewer than MinPts within eps but is a neighbor of a core point.
    3. **Noise or Outlier**: Neither a core nor a border point.
![image](https://github.com/Kiranwaghmare123/PG-DBDA-MAR2024/assets/72081819/cb4060ef-3a80-4a93-9d32-5714bf5bc355)

 #### Steps in DBSCAN Algorithm
    1. **Identify Core Points**:
       - Find neighbors within eps for each point.
       - Mark points with ≥ MinPts neighbors as core points.
       
    2. **Cluster Assignment**:
       - For each core point not already in a cluster, create a new cluster.
       - Recursively find all density-connected points and assign them to the cluster.
       - Density-Connected: Points connected through a chain of core points.
    
    3. **Iterate Through Points**:
       - Visit all points in the dataset.
       - Points not belonging to any cluster are marked as noise.

![image](https://github.com/Kiranwaghmare123/PG-DBDA-MAR2024/assets/72081819/ffb00c33-f621-4441-9f9d-fee1c919e5f7)

### Pseudocode for DBSCAN
    DBSCAN(dataset, eps, MinPts){
        C = 1  # Initialize cluster index
        for each unvisited point p in dataset {
            mark p as visited
            Neighbors N = find neighbors of p
            if |N| >= MinPts:  # If p is a core point
                N = N ∪ N'
                for each point p' in N:
                    if p' is not a member of any cluster:
                        add p' to cluster C
            else:
                mark p as noise
        }
    }


### Visualize the cluster
    y_means = db.fit_predict(X)
    plt.figure(figsize=(7,5))
    plt.scatter(X[y_means == 0, 0], X[y_means == 0, 1], s = 50, c = 'pink')
    plt.scatter(X[y_means == 1, 0], X[y_means == 1, 1], s = 50, c = 'yellow')
    plt.scatter(X[y_means == 2, 0], X[y_means == 2, 1], s = 50, c = 'cyan')
    plt.scatter(X[y_means == 3, 0], X[y_means == 3, 1], s = 50, c = 'magenta')
    plt.scatter(X[y_means == 4, 0], X[y_means == 4, 1], s = 50, c = 'orange')
    plt.scatter(X[y_means == 5, 0], X[y_means == 5, 1], s = 50, c = 'blue')
    plt.scatter(X[y_means == 6, 0], X[y_means == 6, 1], s = 50, c = 'red')
    plt.scatter(X[y_means == 7, 0], X[y_means == 7, 1], s = 50, c = 'black')
    plt.scatter(X[y_means == 8, 0], X[y_means == 8, 1], s = 50, c = 'violet')
    plt.xlabel('Annual Income in (1k)')
    plt.ylabel('Spending Score from 1-100')
    plt.title('Clusters of data')
    plt.show()


### Association Rule Mining
![image](https://github.com/Kiranwaghmare123/PG-DBDA-MAR2024/assets/72081819/e8ee8cf4-8a3a-41ff-8a62-1cd33345eebe)

    1. **Introduction**
       - **Association Rule Mining**: A method to find relationships between variables in large datasets. It is used in various fields, including market basket analysis, bioinformatics, and web usage mining.
       - **Key Terms**:
         - **Itemset**: A collection of one or more items.
         - **Support**: The frequency or occurrence of an itemset in the dataset.
         - **Confidence**: The likelihood that an item Y is also purchased when item X is purchased.
         - **Lift**: The ratio of the observed support to that expected if X and Y were independent.
![image](https://github.com/Kiranwaghmare123/PG-DBDA-MAR2024/assets/72081819/9e02bf4f-bc88-4513-bc50-9522c58b86de)
    
    2. **Frequent Itemset Mining**
       - **Objective**: Identify itemsets that appear frequently in the dataset.
       - **Algorithms**:
         - **Apriori Algorithm**: Iteratively identifies frequent itemsets. It is based on the principle that if an itemset is frequent, all its subsets are also frequent.
         - **FP-Growth Algorithm**: Uses a tree structure to encode the dataset and extract frequent itemsets directly.
    
    3. **Generating Association Rules**
       - **Objective**: Generate rules that predict the occurrence of an item based on the occurrences of other items.
       - **Rule Generation**: From the frequent itemsets, rules of the form `X -> Y` are generated, where X and Y are itemsets.
    
    4. **Evaluation Metrics**
       - **Support**: `Support(X)` is the proportion of transactions in the dataset in which the itemset X appears.
        
       - **Confidence**: `Confidence(X -> Y)` is the proportion of transactions that contain X which also contain Y.
        
       - **Lift**: `Lift(X -> Y)` measures how much more often X and Y occur together than expected if they were statistically independent.
![image](https://github.com/Kiranwaghmare123/PG-DBDA-MAR2024/assets/72081819/7f9f130c-5cb5-47a8-b314-a2474ada6dba)

### Apriri Algorithm
![image](https://github.com/Kiranwaghmare123/PG-DBDA-MAR2024/assets/72081819/d684043c-0e94-4ab6-a782-6dad9b6ba0a0)

### FP Growth Algorithm
![image](https://github.com/Kiranwaghmare123/PG-DBDA-MAR2024/assets/72081819/d34725ba-8250-4e32-9f9d-f0170f833cb4)

### Visualize Rules
    def inspect(results):
        lhs         = [tuple(result[2][0][0])[0] for result in results]
        rhs         = [tuple(result[2][0][1])[0] for result in results]
        supports    = [result[1] for result in results]
        confidences = [result[2][0][2] for result in results]
        lifts       = [result[2][0][3] for result in results]
        return list(zip(lhs, rhs, supports, confidences, lifts))
    resultsinDataFrame = pd.DataFrame(inspect(results), columns = ['Left Hand Side', 'Right Hand Side', 'Support', 'Confidence', 'Lift'])



    for item in results:

    # first index of the inner list
    # Contains base item and add item
    pair = item[0] 
    items = [x for x in pair]
    print("Rule: " + items[0] + " -> " + items[1])

    #second index of the inner list
    print("Support: " + str(item[1]))

    #third index of the list located at 0th
    #of the third index of the inner list

    print("Confidence: " + str(item[2][0][2]))
    print("Lift: " + str(item[2][0][3]))
    print("=====================================")

# EX 1:

    dataset = pd.DataFrame({
        'Transaction': [1, 1, 1, 2, 2, 3, 3, 3],
        'Item': ['Milk', 'Bread', 'Butter', 'Bread', 'Butter', 'Milk', 'Bread', 'Butter']
    })
