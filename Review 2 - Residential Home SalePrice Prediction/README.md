# Review 2: Residential Home SalePrice Prediction & Advanced Machine Learning

## 📋 Problem Statement
> **"Predict the continuous target variable SalePrice for residential homes based on continuous and categorical features such as square footage, neighborhood, and build year."**

---

## 🎯 Project Overview
Accurate real estate valuation requires models that can capture complex interactions between continuous measurements (living area, basement area, lot frontage), temporal indicators (year built, year remodeled), and categorical factors (neighborhood tier, zoning classification, overall material and finish quality).

This project implements rigorous classical and probabilistic machine learning paradigms applied to the official **Kaggle Ames Housing Dataset** (`train.csv`) to predict `SalePrice` and classify homes into market price segments.

---

## 🔬 Core Methodology & Machine Learning Topics Covered

1. **Maximum Likelihood Estimation (MLE) & Ordinary Least Squares (OLS)**:
   - Analytical closed-form normal equation $(\mathbf{X}^T \mathbf{X})^{-1}\mathbf{X}^T \mathbf{y}$ vs. gradient-based optimization.
   - Residual variance and log-likelihood formulations.

2. **Robust & Regularized Regression**:
   - **Ridge Regression ($L_2$) & Lasso Regression ($L_1$)**: Shrinkage and automatic feature selection for high-dimensional multicollinear predictors.
   - **Huber Loss Regression**: Hybrid $L_1/L_2$ piecewise loss function ensuring robustness against high-leverage outliers and luxury anomalies.

3. **Bayesian Linear Regression**:
   - Conjugate Gaussian priors over weights $\mathbf{w} \sim \mathcal{N}(\mathbf{m}_0, \mathbf{S}_0)$.
   - Posterior weight distribution update $\mathbf{w} | \mathcal{D} \sim \mathcal{N}(\mathbf{m}_N, \mathbf{S}_N)$.
   - Analytical predictive distributions delivering epistemic and aleatoric uncertainty intervals for home valuations.

4. **Linear Discriminant & Classification Functions**:
   - Multi-class / binary market tier classification using Fisher’s Linear Discriminant Analysis (LDA) and the classic Rosenblatt Perceptron.

5. **Generative vs. Discriminative Modeling**:
   - **Gaussian Discriminant Analysis (GDA)**: Joint distribution modeling $p(\mathbf{x}, y)$ with shared and class-specific covariance structures.
   - **Logistic Regression**: Direct posterior modeling $p(y|\mathbf{x})$ via sigmoid activation and cross-entropy loss.

6. **Laplace Approximation & Bayesian Logistic Regression**:
   - Second-order Taylor series approximation around the MAP weight vector $\hat{\mathbf{w}}_{\text{MAP}}$ using the Hessian matrix.

7. **Support Vector Machines (SVM)**:
   - Maximum-margin hyperplanes, dual formulation with Lagrange multipliers, and soft-margin hinge loss optimization.
   - Kernel trick evaluation (Linear, Radial Basis Function RBF, Polynomial).

---

## 📁 Implementation File
- **Notebook**: [`House_Price_Advanced_ML.ipynb`](House_Price_Advanced_ML.ipynb)
