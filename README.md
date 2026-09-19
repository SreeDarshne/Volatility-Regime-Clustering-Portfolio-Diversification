# Volatility Regime Clustering and Its Impact on Portfolio Diversification

## Overview

Financial markets do not maintain a constant level of risk. Periods of relative stability are often interrupted by episodes of elevated volatility, during which asset correlations and portfolio risk can change substantially.

This project investigates how **volatility regimes influence portfolio diversification and investment risk**. Rather than assuming constant market conditions, the analysis identifies distinct **low-, medium-, and high-volatility regimes** and examines how asset correlations, portfolio risk, and risk-adjusted performance change across these market states.

The project combines **financial analytics, unsupervised machine learning, rolling-window analysis, correlation analysis, and portfolio risk metrics** to study whether regime-aware portfolio management can provide a more realistic approach to diversification.

---

## Objectives

The primary objectives of the project are to:

- Identify distinct volatility regimes in financial markets.
- Analyze how asset correlations change across market regimes.
- Examine whether diversification benefits weaken during periods of market stress.
- Compare portfolio risk and performance across low-, medium-, and high-volatility environments.
- Investigate the limitations of static portfolio strategies.
- Explore the potential of regime-aware portfolio management for dynamic risk control.

---

## Dataset

The empirical analysis uses historical financial market data covering multiple market cycles.

The study works with daily closing-price data for a collection of financial assets and analyzes market behavior across periods of stability, crisis, and recovery.

The preprocessing pipeline includes:

- Missing-value handling
- Price standardization
- Log-return calculation
- Normalization
- Rolling-window volatility estimation

---

## Methodology

### 1. Financial Data Preprocessing

Historical price data is cleaned and transformed into return series suitable for volatility and portfolio analysis.

Logarithmic returns are calculated to represent changes in asset prices over time.

### 2. Rolling Volatility Estimation

Market volatility is estimated using a **rolling-window approach**.

A rolling volatility measure provides a dynamic representation of market risk and makes it possible to detect periods of elevated and subdued volatility.

The analysis uses a **30-day rolling volatility window** to examine changing market conditions.

### 3. Volatility Regime Detection

The volatility series is analyzed using clustering and regime-detection techniques, including:

- **K-Means Clustering**
- **Gaussian Mixture Models (GMM)**
- **Change-Point Detection**

The market is categorized into three regimes:

- Low Volatility
- Medium Volatility
- High Volatility

This data-driven approach allows market states to be identified from observed volatility behavior rather than relying entirely on predefined thresholds.

### 4. Regime-Based Correlation Analysis

Asset correlation matrices are calculated separately for each volatility regime.

This allows the project to investigate whether relationships between assets remain stable or become stronger during periods of market stress.

### 5. Portfolio Analysis

Portfolio behavior is evaluated separately under different volatility regimes.

The study examines how changing market conditions affect diversification, risk exposure, and portfolio performance.

### 6. Risk and Performance Evaluation

Portfolio performance is evaluated using financial risk and performance metrics including:

- Mean Return
- Volatility
- Sharpe Ratio
- Value at Risk (VaR)
- Portfolio Variance
- Correlation Analysis

---

## Key Results

The analysis identified three structurally different volatility regimes.

### Low-Volatility Regime

The low-volatility regime produced:

- Mean Return: **0.001249**
- Volatility: **0.010065**
- Sharpe Ratio: **0.124109**
- VaR (95%): **-0.016164**
- Portfolio Variance: **0.000101**

Asset correlations were comparatively moderate, providing stronger diversification opportunities.

### Medium-Volatility Regime

The medium-volatility regime produced:

- Mean Return: **0.000719**
- Volatility: **0.019027**
- Sharpe Ratio: **0.037767**
- VaR (95%): **-0.030940**
- Portfolio Variance: **0.000362**

Asset correlations increased as market uncertainty grew, reducing diversification effectiveness.

### High-Volatility Regime

The high-volatility regime produced:

- Mean Return: **0.004706**
- Volatility: **0.045735**
- Sharpe Ratio: **0.102899**
- VaR (95%): **-0.063791**
- Portfolio Variance: **0.002092**

During high-volatility periods, correlations between many assets increased substantially, weakening the protection normally provided by diversification.

---

## Major Findings

### Volatility is Regime-Dependent

The results demonstrate that market risk changes substantially over time rather than remaining constant.

A particularly large volatility spike is observed around the 2020 market disruption, illustrating the clustering of volatility during periods of systemic stress.

### Correlations Increase During Market Stress

Asset correlations generally increase as volatility rises.

During low-volatility periods, asset movements are relatively independent, while high-volatility periods show substantially stronger co-movement.

### Diversification Benefits Are Dynamic

Diversification is more effective during relatively stable market conditions.

During high-volatility regimes, rising correlations reduce the ability of a traditionally diversified portfolio to offset losses across assets.

### Portfolio Risk Increases Sharply

Portfolio variance increased from:

```text
Low Volatility     : 0.000101
Medium Volatility  : 0.000362
High Volatility    : 0.002092
```

The results demonstrate a substantial increase in portfolio risk during turbulent market conditions.

### Downside Risk Also Increases

The 95% Value at Risk changed from:

```text
Low Volatility     : -0.016164
Medium Volatility  : -0.030940
High Volatility    : -0.063791
```

This indicates considerably greater downside exposure during high-volatility regimes.

---

## Portfolio Management Implications

The results highlight a limitation of portfolio strategies that assume constant volatility and correlations.

A regime-aware approach can instead incorporate changing market conditions into portfolio decision-making.

For example, portfolio exposure can potentially be adjusted when the market transitions into a high-volatility regime, where correlations increase and conventional diversification becomes less effective.

This provides motivation for more adaptive approaches to:

- Portfolio allocation
- Risk management
- Stress testing
- Diversification
- Market regime monitoring

---

## Technologies and Concepts

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Scikit-learn
- Financial Time-Series Analysis
- K-Means Clustering
- Gaussian Mixture Models
- Change-Point Detection
- Rolling Volatility
- Correlation Analysis
- Portfolio Analytics
- Sharpe Ratio
- Value at Risk (VaR)
- Portfolio Variance
- Data Visualization

---

## Repository Structure

```text
Volatility-Regime-Clustering-Portfolio-Diversification/
│
├── RFA_REV2.ipynb
│   └── Main analysis notebook
│
├── RFA_PROJECT FINAL REVIEW.docx
│   └── Complete project report and results
│
├── .gitignore
│
└── README.md
```

---

## Limitations

The analysis is based on historical financial data and a specific set of modelling assumptions.

The current study does not fully incorporate factors such as:

- Transaction costs
- Liquidity constraints
- Real-time execution
- Slippage
- Other implementation costs

Therefore, the results should be interpreted as an empirical research analysis rather than a directly deployable investment strategy.

---

## Future Work

Future extensions could include:

- Real-time volatility regime detection
- Hidden Markov Models (HMM)
- GARCH-family volatility models
- Additional asset classes
- Dynamic asset allocation
- Transaction-cost-aware portfolio optimization
- Backtesting regime-switching strategies
- Deep-learning-based regime detection
- Comparison with static benchmark portfolios

---

## Authors

**Daphni Michelle B**  
**Sree Darshne J**  
**Sujana S**

Integrated M.Tech – Computer Science and Engineering  
Specialization in Business Analytics  
Vellore Institute of Technology (VIT), Chennai

---

## Disclaimer

This project was developed for **academic and research purposes**. The analysis and results presented in this repository should not be interpreted as financial or investment advice.
