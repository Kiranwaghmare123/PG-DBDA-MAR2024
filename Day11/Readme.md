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


### Visualize Rules
    def inspect(results):
        lhs         = [tuple(result[2][0][0])[0] for result in results]
        rhs         = [tuple(result[2][0][1])[0] for result in results]
        supports    = [result[1] for result in results]
        confidences = [result[2][0][2] for result in results]
        lifts       = [result[2][0][3] for result in results]
        return list(zip(lhs, rhs, supports, confidences, lifts))
    resultsinDataFrame = pd.DataFrame(inspect(results), columns = ['Left Hand Side', 'Right Hand Side', 'Support', 'Confidence', 'Lift'])
