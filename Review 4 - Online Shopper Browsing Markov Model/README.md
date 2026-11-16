# Review 4: E-Commerce Browsing Sequence Prediction using First-Order Markov Models

## 📋 Problem Statement
> **"Model online shopper browsing sequences across e-commerce categories using first-order Markov models to predict the next page a user will visit based on their immediate transition history, enabling real-time personalized product recommendations."**

---

## 🎯 Project Overview
In fast-paced e-commerce environments, customer sessions are transient and intent frequently shifts within seconds. Traditional static collaborative filtering requires extensive historical user profiles and fails for anonymous first-time visitors or sudden intent drifts.

This project implements a **First-Order Markov Chain** sequential model to represent clickstream journeys across product categories and funnel stages. By conditioning solely on the user's most recent interaction, the system provides instantaneous next-page probability estimation for dynamic, sub-millisecond recommendation routing.

---

## 🔬 Theoretical Foundations & Mathematical Objects

1. **The First-Order Markov Property**:
   A stochastic process $\{S_t, t \ge 0\}$ satisfies the first-order Markov assumption if the conditional probability of the future state depends strictly on the current state:
   $$P(S_{t+1} = j \mid S_t = i, S_{t-1} = i_{t-1}, \dots, S_0 = i_0) = P(S_{t+1} = j \mid S_t = i) = P_{ij}$$

2. **State Space Formulation ($\mathcal{S}$)**:
   - Category navigation states: Home, Electronics, Fashion/Apparel, Home & Kitchen, Books, Beauty, etc.
   - Conversion funnel states: Search, Product Detail Page (PDP), Cart, Checkout, Exit / Session Terminate.

3. **Transition Probability Matrix ($\mathbf{P}$)**:
   - An $M \times M$ row-stochastic matrix where $P_{ij} \ge 0$ and $\sum_{j=1}^M P_{ij} = 1$ for all states $i$.
   - **Maximum Likelihood Estimation (MLE)**:
     $$P_{ij}^{\text{MLE}} = \frac{N_{ij}}{\sum_{k=1}^M N_{ik}}$$
   - **Laplace (Additive) Smoothing**:
     $$P_{ij}^{\text{Laplace}} = \frac{N_{ij} + \alpha}{\sum_{k=1}^M (N_{ik} + \alpha) }$$
     Prevents zero-probability traps for unseen category transitions.

4. **Initial State Distribution ($\boldsymbol{\pi}_0$)**:
   The entry vector defining the probability of session initiation at each state $i \in \mathcal{S}$.

5. **Stationary Distribution ($\boldsymbol{\pi}^*$)**:
   The long-term equilibrium vector satisfying:
   $$\boldsymbol{\pi}^* \mathbf{P} = \boldsymbol{\pi}^*, \quad \text{subject to } \sum_{i} \pi_i^* = 1$$
   Reveals site-wide traffic balance and fundamental category gravity.

6. **Real-Time Recommendation Engine**:
   - Given active state $S_t = i$, rank prospective categories $j \in \mathcal{S} \setminus \{\text{Exit}\}$ by conditional transition likelihood $P_{ij}$.
   - Delivers personalized, low-latency banner or widget product suggestions.

---

## 📁 Implementation File
- **Notebook**: [`first_order_markov_ecommerce_executed.ipynb`](first_order_markov_ecommerce_executed.ipynb)
