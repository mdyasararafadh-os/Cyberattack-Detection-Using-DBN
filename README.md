# Cyberattack Behaviour Modelling and Intrusion Detection Using Dynamic Bayesian Networks

## Overview

This project investigates the use of Dynamic Bayesian Networks (DBNs) for modelling network behaviour over time and detecting potentially malicious network activities.

The project uses the UNSW-NB15 network intrusion detection dataset and compares the proposed DBN approach with conventional machine learning models.

## Problem Statement

Traditional intrusion detection approaches may struggle to identify evolving cyberattacks by examining individual network activities.

This project aims to model network behaviour over time using Dynamic Bayesian Networks and identify potentially malicious activities through probabilistic analysis.

## Objectives

- Analyse network traffic data for intrusion detection.
- Model attack behaviour using Dynamic Bayesian Networks.
- Study the relationship between network traffic features and attack labels.
- Compare the DBN model with conventional machine learning models.
- Evaluate model performance using classification metrics.

## Dataset

**Dataset:** UNSW-NB15

The dataset contains network traffic records labelled as normal or attack.

For this project, network records are aggregated by timestamp to create time-based observations. Network traffic features are used to represent the behaviour of each observation.

The dataset files are not included in this repository because of their large size.

## Methodology

1. Data exploration and understanding.
2. Data preprocessing and cleaning.
3. Aggregation of network traffic records by timestamp.
4. Creation of time-based sequences.
5. Discretisation of selected network features.
6. Construction of the Dynamic Bayesian Network.
7. Training and evaluation of baseline machine learning models.
8. Model comparison using classification metrics.

## Models

The following models were evaluated:

- Dynamic Bayesian Network (DBN)
- Logistic Regression
- Random Forest

The DBN is the main model investigated in this project. Logistic Regression and Random Forest are used as comparison models.

## Results

The following results were obtained on the held-out test dataset:

| Model | Accuracy | Precision | Recall | F1-score |
|---|---:|---:|---:|---:|
| Dynamic Bayesian Network | 69.62% | 90.63% | 73.52% | 81.18% |
| Logistic Regression | 74.23% | 90.63% | 79.28% | 84.58% |
| Random Forest | 66.92% | 90.68% | 70.09% | 79.07% |

Logistic Regression achieved the highest F1-score among the evaluated models.

The DBN demonstrated the ability to model probabilistic relationships between network behaviour and attack labels. However, the results also indicate that further improvement is needed, particularly in distinguishing normal traffic from attack traffic.

## Limitations

- The dataset showed a substantial difference in attack proportions between the training and test files.
- The models showed limited ability to correctly identify normal traffic in the test dataset.
- The current DBN uses a simplified one-step temporal inference approach.
- Further work is required to improve generalisation and intrusion detection performance.

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Jupyter Notebook
- Dynamic Bayesian Networks
- Matplotlib / Seaborn

## How to Run

1. Clone or download this repository.
2. Install the required Python libraries.
3. Download the UNSW-NB15 dataset separately.
4. Place the required dataset CSV files in the local `dataset/` folder.
5. Open the notebooks using Jupyter Notebook or VS Code.
6. Run the notebooks in the documented order.

## Future Improvements

- Improve DBN structure and temporal modelling.
- Investigate methods to handle dataset distribution shift.
- Improve normal traffic detection.
- Evaluate the model on additional network traffic datasets.
- Explore real-time intrusion detection.
