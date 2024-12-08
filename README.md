# decision_trees
What is a decision tree?
A decision tree is a non-parametric supervised learning algorithm, which is utilized for both classification and regression tasks. It has a hierarchical, tree structure, which consists of a root node, branches, internal nodes and leaf nodes.

As you can see from the diagram below, a decision tree starts with a root node, which does not have any incoming branches. The outgoing branches from the root node then feed into the internal nodes, also known as decision nodes. Based on the available features, both node types conduct evaluations to form homogenous subsets, which are denoted by leaf nodes, or terminal nodes. The leaf nodes represent all the possible outcomes within the dataset.

![image](https://github.com/user-attachments/assets/577fa841-12c3-4c21-90d7-a533a6e2ce4a)

## Steps to Build a Decision Tree Model

### 1. Understand the Problem
- Identify whether the task is **classification** (categorical output) or **regression** (continuous output).

### 2. Prepare Data
- Clean and preprocess data.
- Handle missing values and categorical features.
- Split the dataset into training and testing sets.

### 3. Choose the Algorithm
- **Classification and Regression Trees (CART)** is commonly used.
- Advanced algorithms like **Random Forest** or **Gradient Boosted Trees** (e.g., XGBoost) can enhance performance.

### 4. Train the Model
- Use a decision tree library (e.g., `scikit-learn`) to train the model on the training data.
- Optimize splitting criteria like **Gini Impurity** (classification) or **Mean Squared Error (MSE)** (regression).

### 5. Prune the Tree
- Pruning reduces overfitting by limiting tree depth or using post-pruning techniques.

### 6. Evaluate the Model
- Measure performance on test data using metrics like:
  - **Accuracy**, **Precision/Recall** (for classification)
  - **Root Mean Squared Error (RMSE)** (for regression)

### 7. Fine-Tune Hyperparameters
- Adjust parameters such as:
  - `max_depth`
  - `min_samples_split`
  - `max_features`

## Key Hyperparameters

- `criterion`: The function to measure the quality of a split (`'gini'` or `'entropy'` for classification, `'mse'` for regression).
- `max_depth`: The maximum depth of the tree.
- `min_samples_split`: The minimum number of samples required to split a node.
- `min_samples_leaf`: The minimum number of samples required in a leaf node.

---

## Advanced Approaches

- **Random Forest**: Builds multiple decision trees and aggregates their results for better generalization.
- **Gradient Boosted Trees**: Sequentially builds trees to minimize errors from previous ones.
- **Hyperparameter Tuning**: Use `GridSearchCV` or `RandomizedSearchCV` to find the optimal configuration.

