# retail_store_inventory
Project Title: Retail Store Inventory Analysis with Random Forest Regression

Overview
This project involves the creation and evaluation of Random Forest Regressor models for predicting the performance of retail store inventory. We evaluated the impact of different numbers of estimators on model performance and plotted various graphs to analyze the correlation between different parameters.

Content
1. Model Creation

1.1 Model 1: Random Forest Regressor with 50 Estimators

reg_model = RandomForestRegressor(n_estimators=50, random_state=44)
reg_model.fit(X_train, y_train)
print("Train Score: ", reg_model.score(X_train, y_train))
print("Test Score: ", reg_model.score(X_test, y_test))

Train Score: 0.9989
Test Score: 0.9927

1.2 Model 2: Random Forest Regressor with 10 Estimators

reg_model2 = RandomForestRegressor(n_estimators=10, random_state=44)
reg_model2.fit(X_train2, y_train2)
print("Train Score: ", reg_model2.score(X_train2, y_train2))
print("Test Score: ", reg_model2.score(X_test2, y_test2))

Train Score: 0.9975
Test Score: 0.9856

2. Model Evaluation
The results show that as the number of estimators increases, both training and test scores improve, indicating better model performance with higher estimators.

Key Observations:

Model 1 with 50 estimators yields a train score of 0.9989 and a test score of 0.9927.
Model 2 with 10 estimators has a train score of 0.9975 and a test score of 0.9856.

3. Data Exploration and Visualization
To analyze the correlation between different parameters in the dataset retail_store_inventory, various visualizations were created, including:

Heatmaps to visualize correlation between numerical features.
Pairplots to examine scatter plots of relationships between pairs of features.

3.1 Heatmap Visualization

corr_matrix = df.corr()
plt.figure(figsize=(10, 8))
sns.heatmap(corr_matrix, annot=True, cmap="coolwarm", fmt=".2f", cbar=True)
plt.title("Correlation Heatmap")
plt.show()

3.2 Pairplot Visualization

sns.pairplot(df)
plt.show()
These visualizations provide insights into the relationships between different features such as Inventory Level, Units Sold, and other key attributes in the dataset.

Conclusion
This project demonstrates the use of Random Forest Regression for inventory management prediction, along with data visualization to better understand parameter correlations.
