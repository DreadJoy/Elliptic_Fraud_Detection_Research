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

### In Progress

* [ ] 02_Baseline_Machine_Learning.ipynb

### Planned

* [ ] 03_Graph_Feature_Engineering.ipynb
* [ ] 04_Graph_Neural_Networks.ipynb
* [ ] 05_Topological_Data_Analysis.ipynb

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

---

## Future Directions

* Compare baseline machine learning models
* Engineer graph-theoretic features
* Explore Graph Convolutional Networks (GCNs)
* Investigate persistent homology and topological features
* Compare classical machine learning against graph-based approaches

---

## References

* Elliptic Bitcoin Dataset
* Anti-Money Laundering in Bitcoin
* Bitcoin Heist (Akcora et al.)
* EvolveGCN (Pareja et al.)
