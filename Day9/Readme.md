# Helper function to plot decision boundaries
       def plot_decision_boundary(X, y, model):
        h = .02  # step size in the mesh
        x_min, x_max = X[:, 0].min() - 1, X[:, 0].max() + 1
        y_min, y_max = X[:, 1].min() - 1, X[:, 1].max() + 1
        xx, yy = np.meshgrid(np.arange(x_min, x_max, h), np.arange(y_min, y_max, h))
        Z = model.predict(np.c_[xx.ravel(), yy.ravel()])
        Z = Z.reshape(xx.shape)
        plt.contourf(xx, yy, Z, alpha=0.8)
        plt.scatter(X[:, 0], X[:, 1], c=y, edgecolors='k', marker='o')
        plt.xlabel('Feature 1')
        plt.ylabel('Feature 2')
        plt.show()

    # For 2D data
    X_2d = X_train[:, :2]  # Using only the first two features for visualization
    svm_model_2d = SVC(kernel='linear')
    svm_model_2d.fit(X_2d, y_train)
    plot_decision_boundary(X_2d, y_train, svm_model_2d)
    
# Ex 1: 
    # The problem statement
    In this project, I try to classify a pulsar star as legitimate or spurious pulsar star. The legitimate pulsar stars form a minority positive class and spurious pulsar stars form the majority negative class. I implement Support Vector Machines (SVMs) classification algorithm with Python and Scikit-Learn to solve this problem.
    
    To answer the question, I build a SVM classifier to classify the pulsar star as legitimate or spurious. I have used the Predicting a Pulsar Star dataset downloaded from the Kaggle website for this project.
    
    # Dataset description
    I have used the Predicting a Pulsar Star dataset downloaded from Dataset folder.
    
    Pulsars are a rare type of Neutron star that produce radio emission detectable here on Earth. They are of considerable scientific interest as probes of space-time, the inter-stellar medium, and states of matter. Classification algorithms in particular are being adopted, which treat the data sets as binary classification problems. Here the legitimate pulsar examples form minority positive class and spurious examples form the majority negative class.
    
    The data set shared here contains 16,259 spurious examples caused by RFI/noise, and 1,639 real pulsar examples. Each row lists the variables first, and the class label is the final entry. The class labels used are 0 (negative) and 1 (positive).
    
    # Attribute Information:
    Each candidate is described by 8 continuous variables, and a single class variable. The first four are simple statistics obtained from the integrated pulse profile. The remaining four variables are similarly obtained from the DM-SNR curve . These are summarised below:
    
    Mean of the integrated profile.
    
    Standard deviation of the integrated profile.
    
    Excess kurtosis of the integrated profile.
    
    Skewness of the integrated profile.
    
    Mean of the DM-SNR curve.
    
    Standard deviation of the DM-SNR curve.
    
    Excess kurtosis of the DM-SNR curve.
    
    Skewness of the DM-SNR curve.
    
    Class
