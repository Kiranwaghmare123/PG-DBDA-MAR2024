# Ex 1:
    data = {
        'age': [25, 35, 45, 55, 65, 75, 85, 95, 26, 36, 46, 56, 66, 76, 86, 96, 27, 37, 47, 57, 67, 77, 87, 97, 28, 38, 48, 58, 68, 78, 88, 98],
        'experience': [1, 3, 5, 7, 9, 11, 13, 15, 2, 4, 6, 8, 10, 12, 14, 16, 3, 5, 7, 9, 11, 13, 15, 17, 4, 6, 8, 10, 12, 14, 16, 18],
        'salary': [50000, 60000, 80000, 110000, 150000, 200000, 250000, 300000, 52000, 62000, 82000, 112000, 152000, 202000, 252000, 302000, 54000, 64000, 84000, 114000, 154000, 204000, 254000, 304000, 56000, 66000, 86000, 116000, 156000, 206000, 256000, 306000]
    }


# Ex 2:
    data = {
        'age': [25, 35, 45, 55, 65, 75, 85, 95],
        'experience': [1, 3, 5, 7, 9, 11, 13, 15],
        'salary': [50000, 60000, 80000, 110000, 150000, 200000, 250000, 300000]
    }

# Ex 3: Optimization parameter value
    parameters={'alpha' : [1,5,10,20,35,45,50,55,60,75,80,95,100]}
    use GridSearch()
    
# Ex 4:

    np.random.seed(0)
    X = 6 * np.random.rand(100, 1) - 3
    y = 0.5 * X**2 + 1.5 * X + 2 + np.random.randn(100, 1)


# Solution: Those who are not able to get coefficients, follow the given code:

''' python
df = pd.read_csv('BostonHousing.csv')
df

X = df.drop('medv', axis=1).values
y = df['medv'].values

scaler = StandardScaler()
X_scaled = scaler.fit_transform(X)

X_train, X_test, y_train, y_test = train_test_split(X_scaled, y, test_size=0.2, random_state=0)

lr = LinearRegression()
lr.fit(X_train, y_train)
y_pred_lr = lr.predict(X_test)
mse_lr = mean_squared_error(y_test, y_pred_lr)
r2_lr = r2_score(y_test, y_pred_lr)
coeff_lr = lr.coef_
coeff_lr

coefficients = pd.Series(coeff_lr, index=df.columns[:-1])
coefficients

coefficients.plot(kind='bar')
'''
