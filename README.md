# Customer Segmentation Using K-Means Clustering

## Project Overview
This project applies **K-Means clustering** to segment mall customers based on their **annual income** and **spending score**. The goal is to identify distinct customer groups for targeted marketing strategies.

## Dependencies
Install required libraries via pip:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

## Dataset
- **File Path**: `../dataset/Mall_Customers.csv`
- **Key Features Used**:
  - `Annual Income (k$)`
  - `Spending Score (1-100)`

## Code Workflow
1. **Data Loading & Inspection**  
   Load the dataset and perform basic analysis (summary statistics, data types).

2. **Feature Selection**  
   Isolate `Annual Income (k$)` and `Spending Score (1-100)` for clustering.

3. **Data Visualization**  
   - Scatter plot of raw data to observe initial patterns.
   - Elbow method plot to determine optimal clusters (\(k=5\)).

4. **Data Scaling**  
   Normalize features using `StandardScaler` to ensure equal weighting.

5. **K-Means Clustering**  
   Train the model with \(k=5\) clusters and assign labels to data points.

6. **Results Visualization**  
   Plot clustered data to visualize customer segments.

7. **Model Evaluation**  
   Calculate Silhouette Score (\(0.70\) for \(k=5\)) to validate cluster quality.

## Key Results
- **Optimal Clusters**: 5 clusters identified via the elbow method, validated by a **Silhouette Score of 0.70** (indicating well-separated, cohesive groups).  
- **Segmentation**: Clear separation of customer groups in the 2D plot, with each cluster corresponding to a distinct behavioral profile:  
  - **Cluster 1 (Orange)**: High-income, low-spending customers (top-left: high income, low spending score).  
  - **Cluster 3 (Pink)**: High-income, high-spending customers (top-right: high income, high spending score).  
  - **Cluster 0 (Teal)**: Medium-income, medium-spending customers (center: balanced income and spending).  
  - **Cluster 4 (Green)**: Low-income, low-spending customers (bottom-left: low income, low spending score).  
  - **Cluster 2 (Blue)**: Low-income, high-spending customers (bottom-right: low income, high spending score).  
- **Validation**: Silhouette Score of \(\boldsymbol{0.70}\) confirms robust cluster quality (scores >0.5 indicate meaningful separation; scores closer to 1 denote stronger cohesion).

## How to Run
1. Place `Mall_Customers.csv` in the `dataset/` folder.
2. Execute the script to generate visualizations and cluster labels.

## Cell Outputs
- `Customer Segmentation Raw Dataset.png`: Initial data distribution.
- `Elbow Method.png`: Inertia plot for cluster selection.
- `Customer Segmentation on Scaled Dataset.png`: Final clustered result.
- Console output: Silhouette Score and cluster assignments.