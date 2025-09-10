# Branch Benchmark

<img width="1610" height="638" alt="image" src="https://github.com/user-attachments/assets/99b577a5-fa2e-401b-9c3a-5d6a2eb7ff99" />

The Branch Benchmark is a machine learning (unsupervised learning) and data science based tool to explore similarities between stores and detect outliers. This advances the understanding of the subject matter experts (SME) about their business.

This approach is a general one; I hope it inspires others to toy with the creation of benchmarks, be it store, group or market comparisons.

# Table of Contents

* [Key Features](#key-features)
* [Tech Stack](#tech-stack)
* [Workflow](#workflow)
  * [Initial Preparation by SMEs](#initial-preparation-by-smes)
  * [Data Preprocessing](#data-preprocessing)
  * [Modeling](#modeling)
  * [From Clustering to Benchmarking](#from-clustering-to-benchmarking)
* [Setup](#setup)
* [License](#license)

# Key Features

The new benchmarking tool is designed to be powerful yet straightforward, allowing you to gain actionable insights from your stores without needing a deep technical background.

The benchmark is EASY TO USE and let's SMEs work with familiar Excel files which are automatically converted into the highly efficient format .parquet. SMEs define their own KPIs on which the benchmark is based. The system is built for SCALABILITY; by using the efficient .parquet data format, it's ready to handle much larger datasets on powerful platforms like Databricks as your needs grow. The true ADDED VALUE lies in its intelligent analysis. Not only does it cluster similar stores, but it also detects outliers with a dendrogram.

# Tech Stack

**Algorithms:**
* scikit-learn for hard clustering (k-Means)
* scikit-fuzzy for soft clustering (Fuzzy c-Means)

**Data:**
* Excel to get inputs from SMEs
* Parquet for fast and efficient data handling

**Development & Isolation:**
* Python scripts
* Jupyter Notebooks
* Anaconda

# Workflow

## Initial Preparation by SMEs
* Excel (the KPIs are provided in a standard Excel file with the axes KPIs & stores)
* Feature Selection: the SMEs ensure a plausible kpi set, relevant to the benchmark
* Feature Store: Execution of the data appender (Python) to save relevant data in a feature store
 
## Data Preprocessing
* Data Cleaning & Data Quality Assessment with YData Profiling
* Feature Engineering: Dimensionality Reduction with correlation matrix & heatmap dendrogram
* Anomaly Detection with boxplots
* Data Transformation with the Yeo-Johnson-function to get an approximation of a normal distribution
* Data Scaling with the robust scaler highly relevant for the selected Euclidean distance

## Modeling
* Hard Cluster (k-Means)
  * Hyperparameter tuning with comparison of elbow-method & silhouette score 
* Soft Cluster (Fuzzy c-Means)
  * Hyperparameter tuning with fuzzy partition coefficient

## From Clustering to Benchmarking
* Measuring Performance: Compare a defined KPI of a defined store with the average of its group (cluster)
* Outlier Detection with a dendrogram

# Setup
A notebook will be uploaded on Kaggle soon. If there is demand, I will create a demo to demonstrate the approach how such a benchmark can be created.

# License
The benchmark is licensed under the GNU General Public License v3. It promotes collaboration and open source software.
