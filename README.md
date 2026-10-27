# Aggregate Risk and Economic Capital

**Collective risk modeling, Monte Carlo simulation and risk management**

## Overview

This project develops a quantitative framework for modeling aggregate insurance losses and measuring portfolio risk. It combines claim frequency and severity distributions with Monte Carlo simulation to estimate Value-at-Risk (VaR), Tail Value-at-Risk (TVaR) and economic capital. It also investigates the effects of dependence, portfolio diversification and reinsurance on aggregate losses.

## Objectives

- Model claim frequency and individual claim severity.
- Simulate aggregate insurance losses using a collective risk model.
- Estimate VaR, TVaR and economic capital at different confidence levels.
- Analyze the impact of dependence and diversification on portfolio risk.
- Evaluate excess-of-loss reinsurance strategies.
- Assess simulation convergence and the sensitivity of risk measures to model assumptions.
- Build an interactive Streamlit application for portfolio risk analysis.

## Data

The project can use a synthetic insurance portfolio calibrated from the `freMTPL2freq` and `freMTPL2sev` datasets developed by CASdatasets, reusing the frequency and severity modeling framework from the motor insurance pricing project.

Alternatively, it can rely on publicly available educational resources from the Casualty Actuarial Society (CAS).

Data sources:

- [CASdatasets — freMTPL2](https://dutangc.github.io/CASdatasets/reference/freMTPL.html)
- [Casualty Actuarial Society — Research Resources](https://www.casact.org/publications-research/research-resources)

See [`data/README.md`](data/README.md) for data provenance, access instructions, portfolio construction, variable definitions and simulation assumptions.

## Methodology

1. Define the insurance portfolio and calibrate claim frequency and severity distributions.
2. Implement a collective risk model combining claim counts and individual claim amounts.
3. Simulate aggregate losses using Monte Carlo methods.
4. Calculate VaR, TVaR and economic capital at multiple confidence levels.
5. Analyze dependence structures and diversification effects across portfolios.
6. Model excess-of-loss reinsurance and compare gross and net risk measures.
7. Assess simulation convergence and perform sensitivity analyses.

## Evaluation

The analysis considers the consistency of simulated losses with theoretical moments, the stability of Monte Carlo estimates and the sensitivity of VaR and TVaR to the number of simulations and confidence levels.

Additional analyses compare independent and dependent portfolios, assess diversification benefits, and quantify the impact of reinsurance on aggregate losses and economic capital.

## Application

The Streamlit application allows users to configure portfolio parameters, select frequency and severity distributions, run Monte Carlo simulations, compare risk measures and visualize the effects of diversification and reinsurance.

## Installation

```bash
git clone https://github.com/YOUR-PSEUDO/aggregate-risk-economic-capital.git
cd aggregate-risk-economic-capital
python -m venv .venv
pip install -r requirements.txt
```

Activate the virtual environment before installing dependencies. See the setup instructions for your operating system.

## Project structure

- `notebooks/`: portfolio calibration, simulation and risk analysis
- `src/`: reusable distribution, simulation, risk measurement and reinsurance modules
- `tests/`: automated tests
- `app/`: interactive Streamlit application
- `reports/`: results, figures and analysis
- `docs/`: methodology, assumptions and limitations

## Limitations

Risk estimates depend on the selected frequency and severity distributions, dependence assumptions and simulation methodology. Extreme-loss estimates may be particularly sensitive to tail assumptions and Monte Carlo sampling variability.

The economic capital measure is defined for educational purposes as VaR minus expected aggregate losses under a specified confidence level. The framework is not a complete regulatory Solvency Capital Requirement (SCR) calculation and does not replace a comprehensive insurance risk management process.

## Author

Toussaint B., Fathnelle M.

## License

See [`LICENSE`](LICENSE).
