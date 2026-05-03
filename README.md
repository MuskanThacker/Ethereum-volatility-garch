# Ethereum Volatility Modeling using GARCH Family Models (Python)

GARCH-based modeling of Ethereum returns to analyze volatility clustering and persistence in crypto markets (Python)

## Project Overview:
This project analyzes the time-varying volatility of Ethereum returns using multiple models from the GARCH family — GARCH, TGARCH and EGARCH.

Cryptocurrency markets are known for high volatility and asymmetric responses to shocks. This study compares different volatility models to identify which best captures Ethereum’s return dynamics.

## Objectives:
- Examine volatility patterns in Ethereum returns  
- Model conditional variance using GARCH-type models  
- Capture asymmetry in volatility (leverage effects)  
- Compare model performance and identify the best fit (in this case it's EGARCH)  

## Methodology:

### 1. Data Preparation
- Collected Ethereum price data  
- Computed **log returns** for analysis  
- Checked basic statistical properties  

### 2. Model Estimation
The following models were estimated:

- **GARCH(1,1)** → captures volatility clustering  
- **TGARCH (Threshold GARCH)** → captures asymmetric response to positive vs negative shocks  
- **EGARCH (Exponential GARCH)** → models volatility in log form and captures asymmetry without non-negativity constraints  

### 3. Model Evaluation
Models were compared using:
- Log-likelihood  
- Information criteria (AIC/BIC)  
- Ability to capture volatility clustering and asymmetry
- 
## Key Results & Insights
- Ethereum returns exhibit strong **volatility clustering**  
- Evidence of **asymmetric volatility** — negative shocks impact volatility differently than positive shocks  
- Standard GARCH captures persistence but fails to fully capture asymmetry  
- TGARCH improves asymmetry modeling but remains limited  

###  Best Model: EGARCH
- **EGARCH outperforms other models** in capturing both persistence and asymmetry  
- It handles volatility dynamics more flexibly due to its logarithmic specification  
- Provides a better fit for crypto market behavior  

## Model Interpretation Notes
- High persistence observed (α + β close to 1 in GARCH-type models)  
- Indicates **slow decay of volatility shocks**  
- Highlights risk and unpredictability in crypto markets  

## Tools & Libraries
- Python  
- `pandas` → data handling  
- `numpy` → numerical computation  
- `arch` → volatility modeling  
- `matplotlib`, `seaborn` → visualization  

## Project Structure
- `GARCH_Ethereum.ipynb` → full analysis and model comparison  
---

## How to Run
1. Open the notebook in Jupyter Notebook / Google Colab  
2. Run code
3. import the data file "crypto_volatility_dec2025_FINAL_2025-12-09.csv"
