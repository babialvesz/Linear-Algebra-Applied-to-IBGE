**Socioeconomic Analysis & Clustering of Brazilian Capitals (2026)**
📌 **Project Overview**
This project performs a multidimensional analysis of socioeconomic indicators across all 27 Brazilian capitals. By combining Exploratory Data Analysis (EDA) with Unsupervised Machine Learning (K-Means Clustering), the study identifies structural patterns and economic hierarchies that define the Brazilian urban landscape.
🎯 **Objectives**
Data Consolidation: Clean and merge disparate datasets (GDP, Gini Index, Unemployment, and Schooling) into a unified analytical structure.
Dimensionality Reduction: Use PCA to understand the "vectors" of similarity between cities.
Automated Categorization: Apply K-Means to formalize city clusters based on structural performance rather than just geographic location.
🛠️ **Tech Stack**
SQL (SQLite/DBeaver): Initial ETL and feature engineering (e.g., anonymization and KPI calculation).
Python: Core environment for data manipulation.
Pandas: Data cleaning and dataframe consolidation.
Scikit-Learn: Implementation of StandardScaler for normalization and KMeans for clustering.
Matplotlib/Seaborn: Advanced data visualization and cluster plotting.
🚀 **Methodology**
1. ETL & Data Preprocessing
The raw data was processed to handle encoding issues and inconsistent naming conventions (such as the trailing backslashes found in initial CSV reads). All monetary and social indicators were consolidated into a master dataframe: df_consolidado.
2. Feature Scaling
Since GDP (Billions) and Unemployment Rates (Percentages) operate on vastly different scales, I applied StandardScaler (Z-score normalization). This step was crucial to prevent high-magnitude variables from biasing the K-Means distance calculations.
3. K-Means Clustering
Based on the Elbow Method, I determined that 3 clusters provided the optimal balance between granularity and interpretability.
📊 **Key Findings & Results**
Based on the centroids and the final cluster distribution, three distinct profiles emerged:
Cluster 1 (The Global Outlier - São Paulo): The model isolated São Paulo as a unique entity. Its massive GDP ($1.06 \times 10^9$) and high schooling levels ($5.59 \times 10^6$) place it in a category of its own, far removed from other Brazilian capitals.
Cluster 2 (Administrative & Economic Hubs): Including cities like Brasília and Rio de Janeiro, this group shows high wealth generation but faces significant challenges with inequality (Gini) and unemployment.
Cluster 0 (Regional Capitals): The core of the country (24 cities, including Recife and Belém). These cities show a more balanced, albeit smaller-scale, socioeconomic structure.
📂 **Project Structure**
Plaintext
├── data/               # Consolidated CSV files
├── notebooks/          # Google Colab notebooks with step-by-step code
├── images/             # Cluster plots and analysis charts
└── README.md           # Project documentation

🏁 **Conclusion**
The analysis confirms that geographic proximity does not always imply socioeconomic similarity. The isolation of São Paulo and the grouping of regional capitals highlight the deep-rooted economic concentration in Brazil.
