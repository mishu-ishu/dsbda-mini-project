# 🏠 Real Estate Price Prediction using Machine Learning and Big Data Tools

## Overview

This project leverages **Machine Learning** and **Big Data technologies** to predict real estate prices per unit area in **New Taipei City, Taiwan**. Using features like house age, MRT distance, number of convenience stores, and geolocation, the project builds a scalable, interpretable system for predicting housing prices. The models implemented include **Linear Regression** and **Decision Tree Regressor**, and are later scaled using **Apache Spark**.

---

## 📌 Objectives

* Develop reliable ML models to predict house prices using structured real estate data.
* Analyze model performance using statistical metrics like MAE, RMSE, and R² Score.
* Implement a scalable pipeline using Apache Spark for large-scale datasets.
* Compare results with existing literature and propose a production-ready architecture.

---

## 🔍 Dataset

* **Source**: UCI Machine Learning Repository
* **Size**: 414 rows, 7 columns
* **Features**:

  * `transaction_date`
  * `house_age`
  * `distance_to_the_nearest_MRT_station`
  * `number_of_convenience_stores`
  * `latitude`, `longitude`
  * `price_per_unit_area` (target)

---

## 🧪 Methodology

1. **Preprocessing**

   * Min-Max scaling
   * Outlier detection via boxplots
   * Train-test split (80:20)

2. **EDA**

   * Distribution plots
   * Correlation heatmaps
   * Summary statistics

3. **Modeling**

   * Linear Regression
   * Decision Tree Regressor
   * Metrics: MAE, RMSE, R²

4. **Big Data Integration**

   * PySpark for scalable data handling
   * MLlib for model training on Spark

5. **Deployment Pipeline**

   * Kafka for ingestion
   * HDFS/S3 for storage
   * Spark for batch/stream processing
   * FastAPI + Docker for serving

---

## 📈 Results Summary

| Model               | MAE  | RMSE | R² Score | Training Time |
| ------------------- | ---- | ---- | -------- | ------------- |
| Linear Regression   | 5.21 | 6.59 | 0.53     | \~0.04 sec    |
| Decision Tree Regr. | 3.98 | 5.32 | 0.70     | \~0.05 sec    |

* Decision Tree performed best, especially in capturing non-linearity.
* Outliers (luxury/low-value homes) introduced minor prediction errors.

---

## 📊 Visualizations (Generated in Colab)

* Feature Importance Plot
* Residual Plot
* Actual vs. Predicted Scatter Plot
* Literature Comparison Table + Bar Graph

---

## 🏗️ Big Data Architecture

![Big Data Architecture Diagram](./images/big_data_architecture.png)

| Stage       | Tool                      |
| ----------- | ------------------------- |
| Ingestion   | Apache Kafka / Flume      |
| Storage     | HDFS / Amazon S3          |
| Processing  | Apache Spark (PySpark)    |
| ML Training | MLlib / XGBoost4J         |
| Serving     | Spark Streaming + FastAPI |

---

## 📚 References

* Yeh, I.C., & Hsu, T.K. (2009). Building real estate valuation models with comparative analysis.
* Zhang, Y. et al. (2015). Real estate valuation using Random Forests.
* UCI Machine Learning Repository: [Link](https://archive.ics.uci.edu/ml/datasets/Real+estate+valuation+data+set)

---

## 🔮 Future Work

* Integrate external datasets (crime rate, school zones, property photos)
* Use deep learning (CNNs for image + RNNs for trends)
* Real-time model updates with user feedback
