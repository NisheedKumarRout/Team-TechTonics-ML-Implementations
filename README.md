# 🚀 Team TechTonics — Machine Learning Implementations

Welcome to the official repository for **Team TechTonics** machine learning project implementations. This repository contains end-to-end implementations, exploratory analyses, probabilistic formulations, and production-grade Jupyter notebooks across five core machine learning reviews.

---

## 📑 Project Index & Review Mapping

| Review | Domain | Problem Statement (Summary) | Primary Model / Paradigm | Folder & Notebook |
| :--- | :--- | :--- | :--- | :--- |
| **Review 1** | **Bike Sharing Demand** | Predict bicycle availability across municipal stations based on usage, time, weather, and commuting patterns. | Exploratory Data Analysis, Time-Series & Spatial Descriptive Statistics | [Review 1 Folder](./Review%201%20-%20Citibike%20Bicycle%20Availability%20Prediction/)<br>`citibike_eda_2014.ipynb` |
| **Review 2** | **Real Estate Valuation** | Predict residential home `SalePrice` using continuous/categorical features and classify market tiers. | MLE, Ridge/Lasso, Huber Loss, Bayesian Regression, LDA, GDA, Logistic, SVM | [Review 2 Folder](./Review%202%20-%20Residential%20Home%20SalePrice%20Prediction/)<br>`House_Price_Advanced_ML.ipynb` |
| **Review 3** | **Customer Segmentation** | Segment retail shoppers into distinct behavioral clusters using transaction history, frequency, and monetary spend (RFM). | Centroid Clustering (K-Means) & Distribution-Based Clustering (GMM / EM) | [Review 3 Folder](./Review%203%20-%20Retail%20Shopper%20Behavioral%20Segmentation/)<br>`Retail_Customer_Segmentation.ipynb` |
| **Review 4** | **E-Commerce Clickstream** | Model browsing sequences across categories with first-order Markov chains to predict next-page visits for recommendations. | First-Order Markov Models, Transition Probability Matrices, MLE, Laplace Smoothing | [Review 4 Folder](./Review%204%20-%20Online%20Shopper%20Browsing%20Markov%20Model/)<br>`first_order_markov_ecommerce_executed.ipynb` |
| **Review 5** | **Microfinance Underwriting** | Understand low-income cash flow fluctuations, allocate suitable credit limits, and predict default risk with inclusion safeguards. | Adaptive CART (Classification & Regression Trees), Cost-Complexity Pruning, Fairness Safeguards | [Review 5 Folder](./Review%205%20-%20Adaptive%20CART%20Microcredit%20Risk%20Prediction/)<br>`Adaptive_CART_Microcredit_Analysis.ipynb` |

---

## 📂 Repository Structure

```text
Team-TechTonics-ML-Implementations/
├── README.md
├── .gitignore
├── Review 1 - Citibike Bicycle Availability Prediction/
│   ├── README.md
│   └── citibike_eda_2014.ipynb
├── Review 2 - Residential Home SalePrice Prediction/
│   ├── README.md
│   └── House_Price_Advanced_ML.ipynb
├── Review 3 - Retail Shopper Behavioral Segmentation/
│   ├── README.md
│   └── Retail_Customer_Segmentation.ipynb
├── Review 4 - Online Shopper Browsing Markov Model/
│   ├── README.md
│   └── first_order_markov_ecommerce_executed.ipynb
└── Review 5 - Adaptive CART Microcredit Risk Prediction/
    ├── README.md
    └── Adaptive_CART_Microcredit_Analysis.ipynb
```

---

## 🛠️ Environment Setup & Installation

To run any of the implementation notebooks locally, ensure you have **Python 3.9+** installed and follow these steps:

### 1. Clone the Repository
```bash
git clone https://github.com/NisheedKumarRout/Team-TechTonics-ML-Implementations.git
cd Team-TechTonics-ML-Implementations
```

### 2. Create and Activate a Virtual Environment
```bash
# Windows
python -m venv venv
.\venv\Scripts\activate

# Linux / macOS
python3 -m venv venv
source venv/bin/activate
```

### 3. Install Required Dependencies
```bash
pip install --upgrade pip
pip install numpy pandas scipy scikit-learn matplotlib seaborn jupyter jupyterlab
```

### 4. Launch Jupyter Notebook / Lab
```bash
jupyter lab
```
Navigate to any of the `Review X` directories and open the `.ipynb` notebook file to execute cells.

---

## 👥 Authors
- **Team**: TechTonics
- **Repository**: [Team-TechTonics-ML-Implementations](https://github.com/NisheedKumarRout/Team-TechTonics-ML-Implementations.git)
