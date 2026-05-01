# Predictive Maintenance – Machine Failure Prediction

## Overview

This project focuses on predicting machine failures using machine learning techniques to enable proactive maintenance and reduce operational downtime. The solution is designed to handle highly imbalanced data and prioritize failure detection.

---

## Problem Statement

Machine failures in manufacturing environments lead to production loss, increased maintenance costs, and operational risks. The objective of this project is to build a predictive model that can identify potential failures in advance, allowing timely intervention.

---

## Dataset

* Highly imbalanced dataset with approximately 1.6% failure cases
* Contains operational features such as:

  * Air temperature
  * Process temperature
  * Rotational speed
  * Torque
  * Tool wear

---

## Approach

### Data Preprocessing

* Removed irrelevant and leakage features
* Cleaned and standardized column names
* Handled class imbalance using class weighting

### Feature Engineering

* Created new features:

  * Power (Torque × Rotational Speed)
  * Wear Ratio (Tool Wear / Speed)
  * Temperature Difference

### Model Development

* Logistic Regression (baseline model)
* Random Forest (improved performance)
* XGBoost (final model)

### Model Optimization

* Hyperparameter tuning using GridSearchCV
* Cross-validation to ensure model stability
* Threshold tuning (0.65) to balance precision and recall

---

## Results

* Improved failure detection recall from 10% to 80%
* Reduced false positives significantly using threshold tuning
* Achieved a practical balance between recall and precision

---

## Model Explainability

* Used SHAP for model interpretation
* Identified key features influencing failure:

  * Torque
  * Tool wear
  * Power

---

## Business Impact

* Enables early detection of machine failures
* Reduces downtime and maintenance costs
* Supports predictive maintenance strategies
* Improves operational efficiency

---

## Tech Stack

* Python
* Pandas, NumPy
* Scikit-learn
* XGBoost
* Matplotlib, Seaborn
* SHAP

---


## Future Improvements

* Deploy model using Streamlit
* Integrate real-time sensor data
* Improve precision using advanced tuning

---

## Conclusion

XGBoost with threshold tuning provided the best performance by effectively balancing failure detection and false alarms. The model is suitable for real-world predictive maintenance applications.
