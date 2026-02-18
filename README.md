# Financial Risk & Forecasting Engine: Monte Carlo Simulation for Southern Company (SO)

## Project Overview
This project provides a robust, data-driven framework for forecasting the future performance of high-cap utility assets. By leveraging 14 years of historical data, this engine simulates 10,000 potential price paths to determine the statistical probability of reaching specific investment targets.

While originally built for equity research, the underlying logic is designed for **operational scalability**, allowing for the forecasting of energy costs, PPA price volatility, and asset generation variance in the renewable energy sector.

## Key Features
* **Automated Data Pipeline:** Extracts historical adjusted close prices directly from financial APIs and processes them into log-returns for time-additive analysis.
* **Probabilistic Modeling:** Utilizes Geometric Brownian Motion (GBM) to calculate **Drift** (long-term trend) and **Volatility** (stochastic noise).
* **Massive-Scale Simulation:** Executes 10,000 randomized iterations across a 252-day trading horizon to identify "tail risks" and confidence intervals.
* **Decision Support Visualization:** Generates distribution histograms and price-path "spider" charts to provide clear visual evidence of risk-adjusted returns.



## Technical Stack
* **Language:** Python 3.9+
* **Libraries:** Pandas, NumPy, Matplotlib, SciPy, yFinance
* **Environment:** Jupyter Notebook / VS Code

## Operational Application (Renewable Energy Context)
This tool demonstrates the core competencies required for **Operations Analysis in Procurement**:
1.  **Forecasting:** The same drift/volatility logic is used to predict energy generation (MWh) and cost variances.
2.  **Scalability:** The script is modular; it can be pointed at any ticker or internal dataset to scale performance analytics across a global portfolio.
3.  **Risk Mitigation:** Provides a "Probability of Success" metric (e.g., probability of a PPA remaining profitable under specific market conditions).

## How to Run
1. Ensure you have the required libraries: `pip install pandas numpy matplotlib yfinance scipy`
2. Open `monte_carlo_engine.ipynb` in VS Code.
3. Select your kernel and click **Run All**.

## Results Analysis
Based on the historical 14-year dataset for Southern Company:
* **Current Price:** $[Insert Price]
* **Target Price:** $76.70
* **Simulation Outcome:** The engine identified a **[X]% probability** of the target price being achieved or exceeded within one trading year.
