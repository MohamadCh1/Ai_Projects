🌍 Unsupervised Learning: Fund Allocation for Countries in Need
📌 Project Overview
HELP International, a humanitarian NGO, has raised $10 million to support countries in dire need. This project applies unsupervised learning techniques to cluster countries based on socio-economic and health indicators, enabling data-driven decisions for strategic fund allocation.
🎯 Objectives
- Cluster countries using numerical features to identify those most in need.
- Compare clustering techniques to determine the most effective segmentation.
- Visualize insights to support transparent and impactful decision-making.
📊 Dataset Summary
- Source: Kaggle – Country Data
- Records: 167 countries
- Features:
- child_mort: Child mortality rate (per 1000 live births)
- exports, imports, health: % of GDP per capita
- income, gdpp: Economic indicators
- inflation, life_expec, total_fer: Development metrics
🔍 Workflow Summary
1. Exploratory Data Analysis (EDA)
- Distribution plots and bar charts to highlight disparities across countries.
- Identification of economically backward nations based on key indicators.
- Boxplots to detect outliers and skewed distributions.
2. Feature Engineering
- Grouped features into thematic categories:
- Health: child_mort, health, life_expec, total_fer
- Trade: exports, imports
- Finance: income, inflation, gdpp
- Normalized and aggregated features to reduce dimensionality and enhance interpretability.
3. Clustering Techniques
- K-Means Clustering: Elbow method and silhouette scores for optimal k.
- DBSCAN: Density-based clustering to detect outliers and core samples.
- Hierarchical Clustering: Dendrogram analysis for hierarchical relationships.
4. Visualization
- 2D and 3D scatter plots using Plotly and Matplotlib.
- Country-level insights for each cluster.
- Highlighted countries at extremes of each feature for targeted aid.
🧠 Key Insights
- African nations consistently rank high in child mortality, fertility, and low GDP.
- Countries like Haiti, Sudan, and Chad emerge as high-priority candidates for aid.
- Trade-heavy nations (e.g., Singapore, Luxembourg) show balanced import-export dynamics.
- Health spending does not always correlate with life expectancy—cultural and systemic factors matter.
📦 Tech Stack
- Python (Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, Plotly)
- Jupyter Notebook
- Data source: Kaggle
🏁 Conclusion
This project demonstrates how unsupervised learning can guide humanitarian aid allocation by uncovering hidden patterns in global development data. The clustering results offer a transparent, scalable framework for prioritizing support where it's needed most.
🙌 Acknowledgments
- Dataset by Rohan0301 on Kaggle
- Inspired by HELP International’s mission
- Visual styling and workflow inspired by best practices in data storytelling
📎 Related Work
- Mall Customer Segmentation – KMeans
- Binary Classification – Titanic
- Time Series Forecasting – Store Sales
