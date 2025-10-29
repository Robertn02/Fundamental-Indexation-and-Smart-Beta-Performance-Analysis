# Fundamental Indexation and Smart Beta Performance Analysis  
### A Fama–French 3-Factor Evaluation (1962–Present)

This project replicates and extends the core empirical results of the *Fundamental Indexation* literature using Fama–French factor data and Compustat/CRSP datasets.  
It evaluates the historical and out-of-sample performance of fundamental weighting schemes — comparing them with traditional market-cap weighting under both **CAPM** and **Fama–French 3-factor models**.

---

## Project Overview

The notebook investigates how fundamental metrics (Book Value, Income, Sales, Dividends) influence portfolio performance relative to market capitalization weighting.  
It follows the academic structure of evaluating performance from **1962–2004 (in-sample)** and **2005–Present (out-of-sample)**, mirroring the design in the original RAFI / Smart Beta studies.

---

## Key Steps

1. **Data Preparation**
   - Load and clean CRSP monthly returns and Compustat annual fundamentals.
   - Merge datasets with appropriate 6-month reporting lag.
   - Integrate Fama–French factors (MKT–RF, SMB, HML, RF).

2. **Portfolio Construction**
   - Construct top-1000 portfolios based on:
     - Market Cap (Reference)
     - Book Equity (SEQ)
     - Income (IB)
     - Sales (SALE)
     - Dividends (DVT)
   - Use t–1 weighting methodology.

3. **Performance Analysis**
   - **Table 1 & 2:** Arithmetic annualized returns, volatility, Sharpe ratios, and excess returns.
   - **Table 3:** CAPM regressions (α, β, t–stats).
   - **Table 4:** Fama–French 3-Factor regressions (α_FF3, β_MKT, β_SMB, β_HML).

4. **Interpretation**
   - Assess persistence of “Smart Beta” performance.
   - Compare in-sample vs. out-of-sample factor exposures.
   - Identify whether fundamental weighting delivers true alpha or just factor tilts.

---

## Insights

- Fundamental-weighted portfolios (Book, Income, Sales) exhibit **positive CAPM alphas** pre-2005.  
- After controlling for **value (HML)** and **size (SMB)** factors, most alphas vanish — confirming returns are **factor-driven, not abnormal**.  
- In the 2005–Present period, “Smart Beta” strategies show **no significant alpha**, reinforcing the view that performance advantages have diminished.

