# Derivative Pricing and No-Arbitrage Analysis

MATLAB-based project focused on derivative pricing, volatility modelling, and no-arbitrage diagnostics using market data.

## Overview

This project implements a full workflow for pricing and analysing derivatives, combining theoretical models with empirical data.  
It covers both classical pricing approaches and more advanced techniques used in quantitative finance.

The goal is to build a consistent framework linking:
- no-arbitrage conditions
- implied volatility modelling
- stochastic simulation
- term structure construction
- structured product valuation

---

## Key Components

### 1. No-Arbitrage Diagnostics
- Verification of Merton bounds
- Monotonicity and convexity checks
- Identification of inconsistencies in option prices

Script: `no_arbitrage_checks.m`


### 2. Implied Volatility Interpolation
- Quadratic regression on implied volatility
- Focus on OTM options
- Estimation of volatility smile

Script: `implied_volatility_interpolation.m`


### 3. Monte Carlo vs Black-Scholes
- Pricing of European options via simulation
- Comparison with analytical Black-Scholes price
- Confidence interval estimation

Script: `monte_carlo_vs_black_scholes.m`


### 4. VSTOXX Estimation (One-Maturity Approach)
- Model-free volatility estimation
- Use of OTM options only
- Implementation of variance replication formula

Script: `vstoxx_one_maturity_estimation.m`


### 5. Interest Rate Modelling
- Empirical distribution fitting (Normal vs Variance Gamma)
- Statistical testing (KS test, Jarque-Bera)
- Tail behaviour analysis

Script: `euribor_distribution_fitting.m`


### 6. OIS Curve Bootstrap
- Construction of risk-free discount curve
- Extraction of zero rates
- Log-linear interpolation of discount factors

Script: `ois_curve_bootstrap.m`


### 7. Structured Product Pricing
- Pricing of a callable bond via Monte Carlo simulation
- Integration of:
  - stochastic underlying (GBM)
  - discount factors (OIS curve)
  - credit risk (CDS bootstrap)
- Pathwise and average-based valuation

Script: `callable_structured_bond_pricing.m`


## Data

The repository includes all datasets required for reproducibility:
- Option data (calls & puts)
- EUROSTOXX50 prices
- VSTOXX data
- EURIBOR rates
- OIS curve data
- CDS spreads (Credit Agricole)


## Methods Used

- Black-Scholes model
- Monte Carlo simulation
- Regression (OLS)
- Bootstrap techniques
- Hazard rate modelling
- Variance Gamma distribution fitting


## How to Run

All scripts are independent and can be run separately in MATLAB.

Some scripts depend on:
- `BSPrice.m`
- datasets included in the repository


## Author

Francesco Melocchi, Simone D'Isabella, Giulio Mazzarella, Alberto Preti


## Notes

This project is intended for academic and research purposes, with a focus on practical implementation of quantitative finance models.
