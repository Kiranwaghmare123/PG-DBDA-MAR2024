Exploratory Data Analysis (EDA) involves visualizing and summarizing data to uncover patterns
, spot anomalies, and test hypotheses. Here are some common diagrams and plots used in EDA:

### 1. Univariate Analysis
#### Histogram
- Used to understand the distribution of a single continuous variable.
```python
sns.histplot(data['variable_name'], kde=True)
plt.title('Histogram of Variable')
plt.show()
```

#### Box Plot
- Used to summarize the distribution of a single continuous variable, showing its central tendency and variability.
```python
sns.boxplot(y=data['variable_name'])
plt.title('Box Plot of Variable')
plt.show()
```

#### Count Plot
- Used for visualizing the count of observations in each category of a categorical variable.
```python
sns.countplot(x=data['categorical_variable'])
plt.title('Count Plot of Categorical Variable')
plt.show()
```

### 2. Bivariate Analysis
#### Scatter Plot
- Used to investigate the relationship between two continuous variables.
```python
sns.scatterplot(x='variable1', y='variable2', data=data)
plt.title('Scatter Plot of Variable1 vs Variable2')
plt.show()
```

#### Heatmap
- Used to display the correlation matrix for multiple variables.
```python
sns.heatmap(data.corr(), annot=True, cmap='coolwarm')
plt.title('Correlation Heatmap')
plt.show()
```

#### Box Plot (Grouped)
- Used to compare the distribution of a continuous variable across different levels of a categorical variable.
```python
sns.boxplot(x='categorical_variable', y='continuous_variable', data=data)
plt.title('Box Plot of Continuous Variable by Categorical Variable')
plt.show()
```

#### Bar Plot
- Used to compare the means or counts of a continuous variable across different categories.
```python
sns.barplot(x='categorical_variable', y='continuous_variable', data=data)
plt.title('Bar Plot of Continuous Variable by Categorical Variable')
plt.show()
```

### 3. Multivariate Analysis
#### Pair Plot
- Used to visualize pairwise relationships and distributions for multiple variables.
```python
sns.pairplot(data)
plt.title('Pair Plot of Data')
plt.show()
```

#### Facet Grid
- Used to plot multiple instances of the same type of plot, separated by the levels of one or more categorical variables.
```python
g = sns.FacetGrid(data, col='categorical_variable1', row='categorical_variable2')
g.map(sns.scatterplot, 'variable1', 'variable2')
plt.show()
```

### 4. Time Series Analysis
#### Line Plot
- Used to visualize data points over time.
```python
sns.lineplot(x='date_variable', y='continuous_variable', data=data)
plt.title('Line Plot of Continuous Variable over Time')
plt.show()
```

### 5. Distribution Analysis
#### KDE Plot (Kernel Density Estimate)
- Used to estimate the probability density function of a continuous variable.
```python
sns.kdeplot(data['variable_name'], shade=True)
plt.title('KDE Plot of Variable')
plt.show()
```

#### Violin Plot
- Combines aspects of a box plot and a KDE plot, showing the distribution of the data and its probability density.
```python
sns.violinplot(x='categorical_variable', y='continuous_variable', data=data)
plt.title('Violin Plot of Continuous Variable by Categorical Variable')
plt.show()
```

### Examples of Code
#### Histograms for Continuous Variables
```python
for col in ['var1', 'var2', 'var3']:
    sns.histplot(data[col], kde=True)
    plt.title(f'Histogram of {col}')
    plt.show()
```

#### Count Plots for Categorical Variables
```python
for col in ['cat_var1', 'cat_var2']:
    sns.countplot(x=data[col])
    plt.title(f'Count Plot of {col}')
    plt.show()
```

#### Pair Plot for Multiple Variables
```python
sns.pairplot(data[['var1', 'var2', 'var3']])
plt.title('Pair Plot of Selected Variables')
plt.show()
```

#### Correlation Heatmap
```python
plt.figure(figsize=(10, 8))
sns.heatmap(data.corr(), annot=True, cmap='coolwarm')
plt.title('Correlation Heatmap')
plt.show()
```

These plots help in understanding the data better and are crucial for identifying trends, 
patterns, and outliers, which can inform further analysis and modeling.
