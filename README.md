# ML-Logistic-Regression

<div align="justify"> 

Classifying cancer cells as either Malignant or Benign helps decide patients treatment path, thereby improving the outcome of the treatments

This notebook provides insights into the analysis of cancer cells, aiming to predict whether a cell is malignant (M) or benign (B) based on its dimensions

Let’s first understand these methodologies

**Logistic regression :** is used for binary classification, where the target variable is binary ( 1 or 0 ). It estimates the probability of the outcome based on the independent variables using a logistic function.

**Forward feature selection :** is used to select the most relevant features for a model. It starts with an empty set of features, and adds one feature at a time to the model based on their contribution to the model's performance. The process is repeated until no further improvement is achieved.

**Steps :**
1. Setup: Import the necessary libraries and load the dataset.
2. EDA: Use `head()`, `info()`, `describe()`, and visualization techniques - histograms, countplots, and boxplots to explore the data.
3. Data Preprocessing:
   - Handles missing values by dropping or imputing them.
   - Converts categorical variables into numerical form using techniques like Label Encoding. Dependent variable Diagnosis is converted to Malignant -1 & Benign - 0.
   - Using Smote to balance the dataset. why am i doing that?

     Having a balanced dataset is crucial for classification problems to prevent bias in the model, as models perform poorly for the minority class. In the notebook , I'm addressing this issue by using SMOTE (Synthetic Minority Over-sampling Technique) for oversampling the minority class ("Benign" in this case)
   - Split the data into predictor variables (X) and the target variable (y).
   - Results from running a full logistic regression implies presence of Multicollineartiy - handle it using VIF
5. Model Training:
   - Split the data into training and testing sets using `train_test_split()` from scikit-learn.
   - Fit the logistic regression model using `LogisticRegression()` from scikit-learn.
6. Model Evaluation:
   - Run a model
        - Full logistic Regression Model on all the columns
        - post addressing multicollinearity
        - With Interaction terms
        - Reduced model - feature selection using FDR
   - Evaluates the performance of the logistic regression model using various metrics - accuracy, precision, recall, F1-score
   - Compare all the models

**Contributions**
Feel free to submit pull requests or start an issue if you find a bug or have any suggestions for improving this notebook.
</div>
