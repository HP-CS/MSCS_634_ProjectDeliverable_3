# MSCS 634: Advanced Data Mining Project Deliverable 3

## Dataset Summary
- **Dataset**: UCI Online Retail
- **Records**: 541,909 rows, 8 attributes
- **Source**: [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Online+Retail)
- **Reason for Selection**: 
  - Real-world transactional dataset suitable for classification, clustering, and association rule mining tasks.
  - Provides rich customer behavior data for pattern discovery.

## Modeling Process

### Classification Models
1. **Decision Tree Classifier**:
   - Baseline model to predict high-spending customers.
   - Achieved good performance with interpretable rules.
2. **k-Nearest Neighbors (k-NN)**:
   - Used hyperparameter tuning (GridSearchCV) to find the optimal number of neighbors.
   - Improved model performance and generalization.

**Evaluation Metrics:**
- Confusion matrix, accuracy, F1 score, and ROC curve were used to compare models.

### Clustering Model
- **K-Means Clustering**:
  - Segmented customers into 3 distinct groups based on their purchasing behaviors.
  - Visualized clusters in a scatter plot, highlighting differences in total quantity and total spending.

### Association Rule Mining
- Applied the **Apriori algorithm** to discover frequent itemsets in customer transactions.
- Generated association rules using lift and confidence thresholds.
- Example pattern: Customers buying *“Gift Set”* often also purchased *“Candle Set”*.

## Key Insights
- **Classification**: Hyperparameter tuning of k-NN improved accuracy over Decision Tree.
- **Clustering**: Identified meaningful customer segments, such as high-frequency low-spenders and infrequent high-spenders.
- **Pattern Mining**: Revealed actionable item associations useful for cross-selling strategies in marketing.

## Challenges and Solutions
- **Imbalanced Classes**: Balanced the dataset using median spending as a threshold for classification.
- **Cluster Interpretability**: Used feature scaling and visualization to understand cluster differences.
- **Sparse Transaction Data**: Filtered infrequent items to improve Apriori performance.

## Files Included
- `Deliverable3_Classification_Clustering_PatternMining.ipynb`: Jupyter Notebook with code, visualizations, and analysis
- `README.md`: This file summarizing the process and findings
