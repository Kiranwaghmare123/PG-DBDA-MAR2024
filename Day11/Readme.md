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
