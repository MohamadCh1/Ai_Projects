🧠 Fake News Clustering with NLP and Unsupervised Learning
This project explores the use of unsupervised machine learning to cluster news statements based on their factual accuracy. By combining natural language processing (NLP), TF-IDF vectorization, dimensionality reduction, and clustering algorithms, we uncover latent patterns in political news and evaluate clustering quality using silhouette scores.
📦 Project Overview
- Goal: Group news statements into meaningful clusters without using labels
- Techniques: Text preprocessing, TF-IDF, PCA, K-Means, Agglomerative Clustering
- Evaluation: Silhouette score comparison and visual inspection
📁 Dataset
- Format: .tsv (tab-separated)
- Labels: true, false, half-true, mostly-true, barely-true, pants-fire
- Preprocessing:
- Dropped irrelevant columns
- Renamed columns to label and news_text
- Balanced dataset to 204 samples (34 per label)
🔧 Pipeline Summary
1. Text Preprocessing
- Lowercasing
- Tokenization
- Stopword removal
- Stemming (PorterStemmer)
- Output stored in preprocessed_news_text
2. Feature Extraction
- TF-IDF vectorization of preprocessed text
- PCA for dimensionality reduction (2D for visualization)
3. Clustering Algorithms
- K-Means Clustering
- Elbow method used to determine optimal clusters (k=6)
- Cluster visualization and centroid plotting
- Agglomerative Hierarchical Clustering
- Dendrogram analysis suggests optimal clusters (k=3)
- Cluster visualization using Ward linkage
4. Evaluation
- Silhouette score computed for both algorithms
- Bar chart comparison of clustering quality
5. Sample Predictions
- Preprocessed and vectorized sample statements
- PCA transformation and cluster assignment
- Demonstrated both single and multi-input predictions
📊 Results
|  |  | 
|  |  | 
|  |  | 


Agglomerative Hierarchical Clustering achieved the highest silhouette score, indicating better-defined clusters for this use case.

🧪 Technologies Used
- Python
- Pandas, NumPy
- NLTK
- Scikit-learn
- Seaborn, Matplotlib
🚀 How to Run
- Install dependencies:
pip install -r requirements.txt

- Place news_data.tsv in your working directory and run the script.
📌 Key Concepts
- TF-IDF: Converts text into weighted numerical features
- PCA: Reduces high-dimensional vectors for visualization
- K-Means: Partitions data into k clusters using centroid optimization
- Agglomerative Clustering: Builds a hierarchy of clusters using linkage methods
- Silhouette Score: Measures how well samples are clustered
📈 Visualizations
- Elbow graph for K-Means
- Dendrogram for hierarchical clustering
- Scatter plots of clustered data with centroids
🧩 Limitations & Future Work
- Clustering does not recover original labels
- PCA may oversimplify semantic relationships
- Future directions:
- Use sentence embeddings (e.g., BERT, SBERT)
- Explore DBSCAN or spectral clustering
- Integrate topic modeling (LDA)
🙌 Acknowledgments
This project was inspired by real-world challenges in misinformation detection. Special thanks to mentors and educators who guided the NLP and clustering journey.
