# Elliptic Fraud Detection Research

Fraud detection research on the Elliptic Bitcoin transaction network using machine learning, graph analytics, temporal validation, and leakage investigation.

## Project Goal

The goal of this project is to investigate fraud detection in Bitcoin transaction networks while emphasizing rigorous validation, graph-based feature engineering, graph neural networks, and topological data analysis.

Rather than focusing only on model performance, this project explores questions such as:

* Is there evidence of data leakage?
* How should temporal validation be performed?
* Which graph features are most informative?
* Can Graph Neural Networks improve performance?
* Can topological features provide additional signal?

---

## Project Roadmap

### Completed

* [x] 01_Leakage_Investigation.ipynb
* [x] 02_Baseline_Machine_Learning.ipynb
* [x] 03_Graph_Feature_Engineering.ipynb
* [x] 04_Static_GNNs.ipynb

### In Progress

* [ ] 05_Temporal_GNNs.ipynb

### Planned

* [ ] 06_Unknown_Class_Experiments.ipynb
* [ ] 07_Final_Model_Comparison.ipynb
* [ ] 08_Topological_Data_Analysis.ipynb

---

## Notebook Overview

### 01_Leakage_Investigation.ipynb

Investigates potential temporal leakage and shortcut signals within the Elliptic dataset using:

* Temporal train/validation/test splits
* Wider temporal gap validation
* Spearman correlation analysis
* KS distribution drift testing
* Mutual information analysis
* Feature ablation experiments
* Label shuffling diagnostics

Main question:

> Is model performance driven by genuine predictive structure or by temporal leakage?

### 02_Baseline_Machine_Learning.ipynb

Builds a clean fraud detection baseline using a strict temporal
train/validation/test split and graph-based features.

Topics include:

- Logistic Regression baseline
- Random Forest baseline
- Degree analysis
- Clustering Coefficient analysis
- PageRank analysis
- Eigenvector Centrality analysis
- Temporal feature behavior
- Feature interpretation and comparison

Main question:

> Which graph features provide useful signal for fraud detection
under a leakage-aware temporal validation framework?

### 03_Graph_Features_Engineering

Investigates whether graph embedding methods provide additional predictive information beyond the original transaction and graph features.
Models evaluated:
- Random Forest
- Node2Vec + Random Forest
- DeepWalk + Randon Forest
- Logistic Regression
- Logisitc Regression + Node2Vec
- Logistic Regression + DeepWalk

Main question:

> Do graph embeddings provide meaningful improvements over the original feature set, or do the existing graph features already capture most of the available structural information?


### 04_Static_GNN

Investigates whether static Graph Neural Networks provide additional predictive information beyond engineered graph features while preserving a temporal train/validation/test evaluation protocol. Models evaluated:
- Graph Convolutional Network (GCN)
- Graph Convolutional Network (Original Features Only)
- GraphSAGE
- GraphSAGE (Original Features Only)

Main question:

> Can static Graph Neural Networks provide meaningful improvements over engineered graph features, or do traditional machine learning approaches remain the stronger baseline for fraud detection?

---

## Future Directions

* Compare baseline machine learning models
* Engineer graph-theoretic features
* Explore Graph Convolutional Networks (GCNs)
* Investigate persistent homology and topological features
* Compare classical machine learning against graph-based approaches

---

## References

* Elliptic Bitcoin Dataset https://www.kaggle.com/datasets/ellipticco/elliptic-data-set
* Anti-Money Laundering in Bitcoin https://arxiv.org/abs/1908.02591
* Bitcoin Heist (Akcora et al.) https://arxiv.org/abs/1906.07852
* EvolveGCN (Pareja et al.) https://arxiv.org/abs/1902.10191
