# ESG Portfolio Optimization with Genetic Algorithms

This project applies a **Genetic Algorithm (GA)** to optimize a portfolio of S&P 500 companies based on their **Environmental, Social, and Governance (ESG)** scores. Developed for the *Topics in Computational Modelling: From Information Theory to Evolutionary Models* course at Università Bocconi, it explores how evolutionary computation techniques can be applied to socially responsible investing.

## Objective

To construct a portfolio of S&P 500 companies that maximizes ESG performance while considering financial return and diversification — using a biologically-inspired optimization method.

## Methodology

A **Genetic Algorithm** was implemented, evolving a population of candidate portfolios across generations. Main steps:

1. **Encoding**: Portfolios are represented as binary vectors selecting companies
2. **Fitness Function**: Combines ESG score, sector diversification, and optional return constraints
3. **Operators**:
   - **Selection**: Tournament selection
   - **Crossover**: One-point crossover
   - **Mutation**: Bit-flip mutation with fixed probability
4. **Termination**: Stops after a fixed number of generations or when improvement plateaus

## File Overview

```bash
project_root/
├── ESG_Portfolio.ipynb                 # Main notebook with GA implementation and results
├── sp500_esg.csv                       # Dataset of S&P 500 companies and ESG scores
├── sp500_esg_ceo_info.csv             # Extended data with CEO, industry, etc.
├── sp500_esg_ceo_info-filtered.csv    # Preprocessed version used in the notebook
└── README.md
```


## Results

- The GA converged to a portfolio with a high average ESG score and diversified sector exposure
- Trade-offs were observed between maximizing ESG scores and maintaining financial diversification
- Multiple runs showed convergence to similar but not identical portfolios, showing the stochasticity of GAs
