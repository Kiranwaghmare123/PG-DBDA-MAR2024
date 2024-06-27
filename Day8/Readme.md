# Visualising the Training data

    from matplotlib.colors import ListedColormap
    X_set, y_set = sc.inverse_transform(X_train), y_train
    X1, X2 = np.meshgrid(np.arange(start = X_set[:, 0].min() - 10, stop = X_set[:, 0].max() + 10, step = 1),
                         np.arange(start = X_set[:, 1].min() - 1000, stop = X_set[:, 1].max() + 1000, step = 1))
    
    plt.contourf(X1, X2, classifier.predict(sc.transform(np.array([X1.ravel(), X2.ravel()]).T)).reshape(X1.shape),
                 alpha = 0.75, cmap = ListedColormap(('blue', 'orange')))
    plt.xlim(X1.min(), X1.max())
    plt.ylim(X2.min(), X2.max())
    for i, j in enumerate(np.unique(y_set)):
        plt.scatter(X_set[y_set == j, 0], X_set[y_set == j, 1], c = ListedColormap(('red', 'green'))(i), label = j)
    plt.title('Naive Bayes (Training set)')
    plt.xlabel('Age')
    plt.ylabel('Estimated Salary')
    plt.legend()
    plt.show()

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
