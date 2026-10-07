# Predictive Modeling of Cart Abandonment in Quick-Commerce Networks

**Course:** Advanced Machine Learning for Business Transformation (AMLBT)  
**Institution:** Goa Institute of Management (PGDM - Big Data Analytics)  
**Team:** Nishant Khandelwal, Anwesha Banerjee, Anisha Saha  

---

## 📌 Project Overview
This repository contains the data, methodology, and code pipeline for our AMLBT project. The core business problem addresses "ghost stockouts" in 10-minute quick-commerce fulfillment networks. When localized demand spikes or supplier lead times fluctuate, high-velocity SKUs deplete rapidly, leading to entire cart abandonments and severe margin leakage. 

Instead of traditional continuous sales forecasting, this project treats inventory depletion as an **operational classification failure**. We built a predictive pipeline using Random Forest and XGBoost to classify the probability of a stockout event during a given replenishment cycle, allowing Q-commerce platforms to dynamically re-route inventory and protect Gross Merchandise Value (GMV).

## 📊 Dataset
The primary data used is the **Inventory and Stockout Optimization Dataset**, simulating daily SKU-level operations across multiple replenishment cycles.
* **Source:** [Kaggle Dataset Link](https://www.kaggle.com/datasets/sergionefedov/inventory-and-stockout-optimization)
* **Note:** Due to GitHub's file size limitations, only a truncated `sample_data.csv` is included in the `/data` directory. To run the full pipeline, download the complete dataset from Kaggle and place it in the `/data` folder.

## 🗂️ Repository Structure
```text
MLBT-Project-/
│
├── data/                   # Contains sample_data.csv (Add full Kaggle .csv here)
├── notebooks/              # Jupyter Notebooks for EDA and baseline model testing
├── src/                    # Modular Python scripts for the ML pipeline
│   ├── data_cleaning.py    # Handles nulls and normalizes lead-time variability
│   └── model_training.py   # GridSearchCV, XGBoost, and evaluation metrics
├── README.md               # Project documentation and reproducibility steps
└── requirements.txt        # Python dependencies
