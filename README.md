# Fraud_Detection_Credit_Card
1. Imports the necessary libraries:
   - `pandas` as `pd`: A library for data manipulation and analysis.
   - `numpy` as `np`: A library for numerical computations.
   - `matplotlib.pyplot` as `plt`: A library for creating visualizations.
   - `seaborn` as `sns`: A library built on top of Matplotlib for creating attractive statistical graphics.
   - Various modules from the `sklearn` (Scikit-learn) library, including `train_test_split` for splitting the data, `StandardScaler` for feature scaling, `LogisticRegression` for logistic regression modeling, `confusion_matrix` for evaluating model performance, and `classification_report` for generating a classification report.

2. Loads the dataset:
   - Reads a CSV file named 'creditcard.csv' using `pd.read_csv()` and stores it in the `data` variable.

3. Performs data cleaning and engineering:
   - Standardizes the 'Amount' column using `StandardScaler()`. It transforms the values of the 'Amount' column to have zero mean and unit variance.
   - Drops the 'Time' column from the dataset using `data.drop()`.

4. Conducts exploratory data analysis (EDA):
   - Prints the shape of the dataset using `data.shape` to display the number of rows and columns.
   - Prints the descriptive statistics of the dataset using `data.describe()` to provide statistical information about the data.
   - Creates a countplot using `sns.countplot()` to visualize the distribution of fraudulent vs. non-fraudulent transactions.
   - Creates a correlation matrix heatmap using `sns.heatmap()` to visualize the correlation between different features in the dataset.

5. Splits the data into training and testing sets:
   - Assigns the features (all columns except 'Class') to the variable `X` and the target variable ('Class') to the variable `y`.
   - Splits the data into training and testing sets using `train_test_split()`. It assigns 80% of the data to training sets (`X_train` and `y_train`) and 20% to testing sets (`X_test` and `y_test`).

6. Trains and tests a logistic regression model:
   - Creates a logistic regression model using `LogisticRegression()` and assigns it to the variable `model`.
   - Trains the model using `model.fit()` with the training data (`X_train` and `y_train`).
   - Predicts the target variable for the testing data using `model.predict()` and assigns the predicted values to `y_pred`.

7. Evaluates the model:
   - Computes the confusion matrix using `confusion_matrix()` by comparing the predicted values (`y_pred`) with the actual values (`y_test`) from the testing data. It stores the result in the variable `cm`.
   - Prints the confusion matrix using `print(cm)`.
   - Prints the classification report using `classification_report()` to provide a detailed evaluation of the model's performance.
   - Creates a heatmap of the confusion matrix using `sns.heatmap()` to visualize the performance of the model.
