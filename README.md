# AI-ML-INTENSHIP-TASK--12
KMeans – Customer Segmentation
#  Customer Segmentation using K-Means Clustering

##  Project Overview
This project performs **customer segmentation** on the Mall Customers dataset using the **K-Means clustering algorithm**.  
Customers are grouped based on their **Annual Income** and **Spending Score**, helping businesses understand purchasing behavior and target customers effectively.

---

##  Dataset
**Mall_Customers.csv**

Key Columns:
- `CustomerID` – Unique customer identifier
- `Annual Income (k$)` – Customer annual income
- `Spending Score (1-100)` – Spending behavior score

---

##  Objective
- Segment customers into meaningful groups
- Identify customer purchasing patterns
- Assist in marketing and business decision-making

---

##  Methodology

### 1️ Data Loading & Inspection
- Loaded the dataset using Pandas
- Inspected income and spending score distributions

### 2️ Data Preprocessing
- Dropped `CustomerID` (not useful for clustering)
- Selected:
  - Annual Income
  - Spending Score
- Applied **StandardScaler** to normalize features

### 3️ Elbow Method
- Ran K-Means for multiple values of K (1–10)
- Stored inertia values
- Plotted the **Elbow Curve**
- Optimal number of clusters identified as **K = 5**

### 4️ K-Means Clustering
- Trained K-Means model with `K = 5`
- Assigned cluster labels to each customer

### 5️ Visualization
- Created scatter plot of:
  - Annual Income vs Spending Score
- Colored points based on cluster labels

---

##  Results & Cluster Interpretation

| Cluster | Description | Customer Type |
|------|-------------|----------------|
| 0 | Low income, low spending | Low-Value Customers |
| 1 | High income, low spending | Careful Customers |
| 2 | Low income, high spending | Impulsive Buyers |
| 3 | High income, high spending | Premium Customers |
| 4 | Average income, average spending | Standard Customers |

---

##  Output Files
- `Mall_Customers_Segmented.csv` – Dataset with cluster labels
- Elbow plot image
- Cluster visualization plot

---

##  Technologies Used
- Python
- Pandas
- Matplotlib
- Scikit-learn

---

##  Conclusion
K-Means clustering successfully segmented customers into 5 distinct groups.  
These insights can be used for:
- Targeted marketing
- Personalized offers
- Customer retention strategies

---

## 📌 Future Enhancements
- Add Age as a third dimension (3D clustering)
- Use Silhouette Score for validation
- Apply DBSCAN or Hierarchical Clustering
