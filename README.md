# Decision Tree Classifier with scikit-learn

## Description
- In this project the [Connect 4](archive.ics.uci.edu/ml/datasets/Connect-4) dataset is used.
- The scikit-learn [DecisionTreeClassifier](https://scikit-learn.org/stable/modules/generated/sklearn.tree.DecisionTreeClassifier.html#sklearn.tree.DecisionTreeClassifier) for classification task (win, draw, loss)
- 3 Different criterions are used in this project **(Entropy, Gini Index and Log loss)**
- The Decision Tree needs to be pruned, so different prunning hyperparameters are tunned to achieve best result (incuding **pre-prunning** and **post-prunning**):
  - **Pre-prunning hyperparameters:**
    - max features: The number of features to consider when looking for the best split
    - max depth: The maximum depth of the tree
    - min samples split: The minimum number of samples required to split an internal node
    - min samples leaf: The minimum number of samples required to be at a leaf node
    - max leaf nodes: Best nodes are defined as relative reduction in impurity
      
  - **Post-prunning hyperparameters:**
    - cost complexity prunning alpha: Minimal cost complexity pruning recursively finds the node with the “weakest link”. The weakest link is characterized by an effective alpha, where the nodes with the smallest effective alpha are pruned first.
- All the best hyperparameters are found both manual and with acikit-learn **GridSearchCV**

The Trees and their evaluations can be found in the notebook attached here.
