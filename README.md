# Data-Driven Prioritization of Rare Diseases Using Orphadata

## Project Overview

This project was completed for the CAPB352 Business Data Analytics Project. The aim of the project is to develop a data-driven prioritisation framework for rare diseases using Orphadata.

The project uses rare disease information such as gene count, age of onset, inheritance patterns, prevalence, and data completeness. The final purpose is to support better decision-making for pharmaceutical research, healthcare resource allocation, and patient advocacy.

## Dataset

The dataset was prepared from Orphadata rare disease files. The original files were combined using SQL and exported as a consolidated dataset:

- `Rare_diseases_summary.csv`

The dataset includes information such as:

- OrphaCode
- Disease name
- DisorderGroup
- gene_count
- onset_count
- inheritance_count
- avg_prevalence

The analysis focuses mainly on **Disorder-level records**, because these records represent specific rare diseases more clearly than broader disease groups or subtypes.

## Project Workflow

The project follows these main steps:

1. Data integration using SQL
2. Data loading and cleaning in Python
3. Missing value and duplicate checks
4. Aggregation-level analysis
5. Filtering to Disorder-level records
6. Exploratory Data Analysis
7. Feature engineering
8. Priority score creation
9. K-Means clustering
10. Hierarchical clustering
11. Gaussian Mixture Models
12. Isolation Forest anomaly detection
13. Random Forest regression for prevalence prediction
14. Exporting final datasets and summary outputs

## Feature Engineering

The following engineered features were created:

- `genetic_complexity_score`
- `clinical_diversity_score`
- `prevalence_signal`
- `data_completeness_score`
- `priority_score`
- `priority_rank`
- `priority_segment`

The priority score combines genetic, clinical, prevalence, and data completeness information to support rare disease ranking.

## Models Used

The project uses the following machine learning and analytical methods:

- K-Means Clustering
- Hierarchical Clustering
- Gaussian Mixture Models
- Isolation Forest
- Linear Regression
- Random Forest Regression

## Main Outputs

The notebook exports several output files, including:

- `rare_diseases_final_prioritization_dataset.csv`
- `priority_summary.csv`
- `cluster_summary.csv`
- `kmeans_validation_metrics.csv`
- `gmm_validation_metrics_all_covariance_types.csv`
- `regression_results.csv`

These outputs can be used for reporting, dashboard-ready analysis, and further decision support.

## Repository Structure

```text
Rare-diseases/
│
├── Data/
│   └── Rare_diseases_summary.csv
│
├── outputs/
│   ├── rare_diseases_final_prioritization_dataset.csv
│   ├── priority_summary.csv
│   ├── cluster_summary.csv
│   ├── kmeans_validation_metrics.csv
│   ├── gmm_validation_metrics_all_covariance_types.csv
│   └── regression_results.csv
│
├── figures/
│   └── project visualisations
│
├── Rare_Disease_Final.ipynb
├── requirements.txt
└── README.md
