# ai-ml-intern_Task-8
Support Vector Machines (SVM)
# Task 8: Clustering with K-Means

## Objective
Perform unsupervised learning using K-Means clustering to group similar data points and evaluate the quality of the clustering.

## Dataset
The dataset used is loaded from a provided CSV or extracted from a ZIP archive. It may contain both categorical and numerical features, which are preprocessed before clustering.

---

## Tools & Libraries
- Python
- Pandas
- Scikit-learn
- Matplotlib
- Seaborn

---

## Steps Performed

### 1. Data Loading & Preprocessing
- Loaded the dataset using `pandas`.
- Checked for null values and performed data cleaning.
- Converted categorical features (like `Gender`) using `pd.get_dummies()` for compatibility with numerical algorithms.

### 2. PCA for Visualization
- Applied **Principal Component Analysis (PCA)** to reduce dimensions to 2D for plotting.
- Visualized the raw data distribution.
- ![image](https://github.com/user-attachments/assets/d2632db9-d16b-4c81-99d8-84e7631b9867)


### 3. K-Means Clustering
- Fit the **KMeans** model on the cleaned data.
- Assigned cluster labels to each data point.
- Handled the memory warning on Windows by setting `OMP_NUM_THREADS=1` if necessary.
-   Cluster
0        2
1        2
2        2
3        2
4        2

### 4. Finding Optimal K using Elbow Method
- Computed **Sum of Squared Errors (SSE)** for `K = 1 to 10`.
- Plotted the **Elbow Curve** to determine the optimal number of clusters.
- ![image](https://github.com/user-attachments/assets/00a9e906-faae-40ab-881c-ec11ede9ddae)


### 5. Cluster Visualization
- Visualized clusters in 2D (PCA-reduced) space.
- Color-coded points by their assigned cluster.
- ![image](https://github.com/user-attachments/assets/b596182a-5b8d-4f63-825f-e4c5a0d3c8b8)


### 6. Evaluation using Silhouette Score
- Calculated **Silhouette Score** to measure clustering quality.
- Printed scores for different `K` values to compare performance.

---

Silhouette Score for K=3: 0.377


## How to Run

1. Make sure you have the required libraries:
   ```bash
   pip install pandas scikit-learn matplotlib seaborn
