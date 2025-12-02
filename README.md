# world-happiness-report-analysis

Database: World Happiness Report
Source: Kaggle(https://www.kaggle.com/datasets)
Domain: socioeconomic indicators

Project is done in a Jupyter Notebook and can be run in PyCharm, Anaconda, or any environment that supports Jupyter notebooks.

DATA VISUALIZATION AND DYNAMIC PRESENTATION

Various visualizations were created using tools such as matplotlib, seaborn and plotly

DATA PREPARATION AND RESEARCH ANALYSIS

There are no missing values ​​so no additional data cleaning is required ie. filling or removing rows/columns with empty values.
Scaling is necessary because different columns have different ranges of values. StandardScaler was used, which standardizes the data so that each characteristic has an average value of 0 and a standard deviation of 1. This enables all attributes to have the same importance in the analysis.

Correlation analysis was then performed in order to reveal mutual relationships between factors (positive or negative relationships). Visualization of correlations was used for a better understanding of the data.
The correlation matrix indicates a high degree of connection between the factors, such as a strong positive correlation between GDP per capita and Healthy life expectancy.

This means that when one grows, the other also grows, and vice versa. These variables can share similar information, which means that their values ​​can predict each other to a certain extent. That is why PCA was used, i.e. data dimensionality reduction.

PCA reduces the dimensionality of the data, retaining as much information as possible. Applying PCA is useful when we have high-dimensional data to reduce complexity and visualize the structure of the data.

HYPOTHESIS TESTING

Hypotheses to test:
Hypothesis 1: There is no significant difference in the average score between the two groups of countries with high and low GDP per capita.
Test: Independent samples t-test (parametric) or Mann-Whitney U test (non-parametric).

Hypothesis 2: The distribution of social support is not normal.
Test: Shapiro-Wilk test to confirm results.

Hypothesis 3: There is a significant correlation between GDP per capita and Score.
Test: Pearson correlation (parametric) and Spearman correlation (non-parametric).

Results:

Hypothesis 1: Difference in score between high and low GDP

T-test: Statistics = 11,231: This is the value of the test-statistic that measures the difference between the average values ​​of Score for two groups (high GDP and low GDP). p-value = 0.000: Since the p-value is significantly less than 0.05, we reject the null hypothesis. This means that there is a significant difference in average Score values ​​between groups with high and low GDP.

Mann-Whitney U test: Stat = 5465,500: This is the value of the U-test statistic used to compare groups without the assumption of normal distribution. p-value = 0.000: As with the T-test, the p-value is very small, confirming a significant difference between the two groups. Conclusion: Countries with high GDP have a significantly higher Score than countries with low GDP. The results of both tests (parametric and non-parametric) are consistent.

Hypothesis 2: Normality testing for Social support

Shapiro-Wilk test: Statistic = 0.907: This value shows a deviation from a normal distribution. p-value = 0.000: Since the p-value is less than 0.05, we reject the hypothesis that the data follow a normal distribution. Conclusion: Social support does not follow a normal distribution. Nonparametric methods should be used for this variable in further analyses.

Hypothesis 3: Correlation between GDP per capita and Score

Pearson Correlation: Coefficient = 0.794: This indicates a very strong positive linear relationship between GDP per capita and Score. p-value = 0.000: A p-value less than 0.05 confirms that this correlation is statistically significant.

Spearman correlation: Coefficient = 0.814: This indicates a very strong monotonic relationship between GDP per capita and Score. p-value = 0.000: Statistically significant correlation, regardless of data distribution. Conclusion: There is a very strong and statistically significant positive relationship between GDP per capita and Score. Countries with a higher GDP usually have a higher score.


PREDICTIVE MODELING AND MACHINE LEARNING

Mean Square Error (MSE) for linear regression: 0.41446413835283513
Metrics for logistic regression:
Accuracy: 0.8125
Precision: 0.7368421052631579
Recall: 0.9333333333333333
F1 score: 0.8235294117647058

ADVANCED MACHINE LEARNING

Techniques used: 
K-means clustering
Decision trees
Perceptrons
Backpropagation

Conclusions:
Decision trees have the best performance in terms of accuracy.
Decision trees have the best balance between precision and responsiveness (F1-score).


Explanation for the success of the model:
Decision trees are easy to interpret and can be fitted to data, but are prone to overfitting.
Neural networks are powerful for complex problems, and back-propagation allows efficient learning of complex patterns, making them suitable for this dataset.
K-means clustering is useful for discovering patterns in data without a target variable and provides additional insights into the structure of a data set.

