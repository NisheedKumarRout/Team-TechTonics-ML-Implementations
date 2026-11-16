# Review 5: Adaptive CART Model for Microcredit Allocation & Loan Default Risk Prediction

## 📋 Problem Statement
> **"Develop an adaptive CART model to understand fluctuations in the cash flow of low-income households, determine suitable microcredit allocation limits, and predict loan default risks while ensuring that vulnerable groups are not excluded."**

---

## 🎯 Project Overview
Access to fair, responsible microcredit is an indispensable catalyst for financial inclusion among low-income households, informal daily-wage workers, and small micro-entrepreneurs. Unlike salaried formal borrowers with predictable earnings and credit bureau scores, vulnerable households face **severe income volatility** (seasonal harvests, casual labor demand) coupled with **unanticipated expenditure shocks** (medical crises, crop failures).

Rigid underwriting models either:
1. **Unfairly exclude creditworthy borrowers** due to temporary cash flow dips (high false positive rate).
2. **Over-allocate debt beyond repayment capacity**, leading to debt distress and delinquency (high false negative rate).

This project constructs an interpretable, fair, and adaptive **Classification and Regression Tree (CART)** framework to address both challenges simultaneously.

---

## 🔬 Core Methodology & Machine Learning Techniques

1. **Cash Flow & Volatility Feature Engineering**:
   - Monthly net cash flow baseline: $\text{Net Cash Flow} = \text{Income} - \text{Essential Expenditures}$.
   - Volatility index & Coefficient of Variation ($CV = \frac{\sigma}{\mu}$) capturing irregular earning intervals.
   - Buffer ratio: Liquid reserves relative to recurring essential outlays.
   - Socioeconomic and household dependency variables ensuring vulnerable segments are represented without bias.

2. **Classification Tree for Default Risk Prediction**:
   - Splitting criteria: **Gini Impurity** and **Information Gain / Entropy**:
     $$I_G(t) = 1 - \sum_{i=1}^C p(i \mid t)^2$$
   - Binary recursive partitioning isolating high-risk cash flow regimes from resilient borrowing profiles.

3. **Regression Tree for Adaptive Credit Allocation Limits**:
   - Splitting criterion: **Mean Squared Error (MSE) / Variance Reduction**:
     $$\Delta \text{Var} = \text{Var}(D) - \left( \frac{|D_L|}{|D|} \text{Var}(D_L) + \frac{|D_R|}{|D|} \text{Var}(D_R) \right)$$
   - Determines customized loan ceilings aligned with conservative, downside-protected debt service capacity rather than optimistic average income.

4. **Cost-Complexity Pruning (Minimal Pruning)**:
   - Cost-complexity measure parameterized by $\alpha \ge 0$:
     $$R_\alpha(T) = R(T) + \alpha |T|$$
   - Cross-validation search over the effective $\alpha$ grid to select optimal subtrees that prevent overfitting while retaining intuitive rule interpretability.

5. **Financial Inclusion & Fairness Safeguards**:
   - Asymmetric loss matrix / cost-sensitive weighting to penalize unfair borrower exclusion.
   - Threshold tuning on default probability scores ensuring vulnerable populations with temporary volatility are provided graduated, low-risk micro-loans rather than blanket rejections.

---

## 📁 Implementation File
- **Notebook**: [`Adaptive_CART_Microcredit_Analysis.ipynb`](Adaptive_CART_Microcredit_Analysis.ipynb)
