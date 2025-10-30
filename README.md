# CreditCardDefault-KNN

=======
# Credit Card Default Prediction with KNN 🤖

This project focuses on predicting whether a credit card client will default next month based on their financial and payment history using the **K-Nearest Neighbors (KNN)** algorithm.

## Dataset 📊
- **File:** `Credit Card Clients.csv`
- **Rows:** 30,000
- **Features:** 23 numeric & categorical features + 1 target column (`default.payment.next.month`)
- **Target:** `default.payment.next.month` → 0 = no default, 1 = default

## Workflow 🛠️

### 1. Data Exploration 🔍
- Checked for **missing values** (none in this dataset).
- Observed the distribution of features like credit limit, age, payment history, bill amounts, and payment amounts.

### 2. Shuffling & Splitting 🔀
- Shuffled the dataset to remove any inherent order.
- Split the data into **training set (80%)** and **test set (20%)**.

### 3. Feature Scaling ⚖️
- Standardized numeric features using `StandardScaler` to ensure all features contribute equally to distance calculation.

### 4. KNN Implementation 🏃‍♂️
- Used **scikit-learn's `KNeighborsClassifier`** with `k = 5`.
- Trained on the scaled training set and predicted defaults on the test set.

### 5. Evaluation 📈
- Compared predictions to actual labels.
- Calculated **accuracy, precision, recall, and F1-score** to evaluate performance.
- Observed model performance for both default and non-default classes.

## Results 🏆
- Accuracy: ~79%
- Precision & Recall:
  - Non-default (0): High precision and recall (~84% & 91%)
  - Default (1): Lower recall (~37%) but moderate precision (~55%)
- Model performs well for non-default cases, while default cases are harder to predict due to class imbalance.
- Scaling features was important for KNN performance.

