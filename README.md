# Anomaly Detection in Credit Card Transactions

This project applies **unsupervised learning** techniques to detect anomalies in a credit card dataset. The workflow includes clustering, distance-based anomaly scoring, and visualization using dimensionality reduction.


### Steps Covered

#### 1. Data Loading & Exploration
- Loaded `credit_card.csv` (10,000 rows, 29 features).
- Checked data info, missing values, and duplicates.
- Verified dataset is clean (no missing or duplicate entries).

#### 2. Clustering with K-Means
- Scaled the data using **StandardScaler**.
- Applied **KMeans clustering** (3 clusters).
- Assigned each record to a cluster.

#### 3. Distance-Based Anomaly Detection
- Calculated distance of each record to its cluster center.
- Defined an anomaly threshold at the **99.6th percentile** of distances.
- Identified **40 anomalies** (outliers).

#### 4. Visualization
- Used **PCA** (2 components) for dimensionality reduction since the dataset has 29 features.
- Visualized clusters and anomalies in 2D space.

### Results 
- The model flagged **40 unusual transactions** out of 10,000.  
- These anomalies represent points that are far from typical customer behavior.  
- This method provides a **data-driven way to highlight potential fraud or rare activity**, but requires further validation to confirm true fraud cases.  

## Tools & Libraries
- Python (Google Colab)
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn (StandardScaler, KMeans, PCA)
- SciPy (distance calculations)
