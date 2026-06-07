# ML-flow_equipment_pipeline
# End-to-End Predictive Maintenance ML Pipeline with MLflow

An enterprise-grade Machine Learning Operations (MLOps) project demonstrating an end-to-end predictive maintenance pipeline. This repository covers automated data generation, exploratory data analysis (EDA), experiment tracking across multiple machine learning models, model registration, lifecycle stage transitions, and production deployment simulations with robust rollback capabilities.

---

## 🚀 Project Overview

The goal of this project is to build a production-ready machine learning system that predicts equipment failure using synthetic sensor data. It systematically tackles two critical phases of production machine learning:
1. **Experiment Tracking (Week 13):** Building data pipelines, logging parameters/metrics, and comparing model performance.
2. **Model Registry & Versioning (Week 14):** Transitioning models through lifecycle stages (`Staging` ➔ `Production`), building real-time inference wrappers, and setting up rollback pipelines.

---

## 🛠️ Tech Stack & Key Libraries
* **MLOps Framework:** MLflow (Tracking Server & Model Registry)
* **Machine Learning:** Scikit-Learn, XGBoost
* **Data Science Stack:** Pandas, NumPy, Matplotlib, Seaborn

---

## 📊 System Architecture & Workflow

1. **Synthetic Sensor Data Generation:** Generates 10,000 equipment entries simulating temperature, vibration, pressure, RPM, and operational age.
2. **Exploratory Data Analysis (EDA):** Evaluates correlations and verifies feature boundaries for anomalous failure indicators.
3. **MLflow Experiment Tracking:** Trains and auto-logs parallel runs for Logistic Regression, Random Forest, and XGBoost models.
4. **Model Registry & Governance:** Registers the optimal run, appends metadata/tags, and transitions the artifact to `Staging`.
5. **Inference Pipeline:** Implements a dynamic production utility fetching the live `Production` version seamlessly.
6. **Rollback Resilience Testing:** Simulates minor-version deployment and instant registry reversion to a previous stable state.

---

## 📂 Repository Structure

```text
├── week13_predictive_maintenance.ipynb   # Part 1: EDA, Pipeline Training, & Experiment Tracking
├── week14_model_registry.ipynb          # Part 2: Model Registration, Staging, & Production Inference
├── README.md                            # Project documentation
└── requirements.txt                     # System dependencies
