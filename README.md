# Random Walk Simulations

Statistical simulations exploring Rademacher distributions and random walk behavior with
varying probabilities.

## Overview

This project implements Monte Carlo simulations to analyze random walks with different 
success probabilities. It compares empirical results against theoretical predictions 
for:

- Rademacher distribution properties (mean, variance)
- Random walk path outcomes (Gambler's Ruin)

## Setup

Install dependencies:

```bash
uv sync
```

## Usage

Run the Jupyter notebook:

```bash
jupyter notebook main.ipynb
```

## Simulations

### I. Rademacher Distribution
Generates M=1000 samples from a Rademacher distribution with p=0.6 and validates 
empirical mean/variance against theoretical values.

### II. Random Walk Visualization
Simulates two random walks starting at S₀=5 until hitting boundaries at 0 or 10, 
visualizing the paths.

### III. Probability Analysis
- **1000 paths (p=0.6)**: Compares theoretical vs. actual bankruptcy/winning frequencies
- **1000 paths (p=0.1)**: Demonstrates high bankruptcy rate with unfavorable odds
- **10,000 paths (p=0.5)**: Fair game analysis showing convergence to 50/50 outcomes

## Key Functions

- `rademacher(M, p)`: Generates M samples from Rademacher distribution
- `random_walk_until(start, until, p)`: Simulates walk until boundary hit
- `theoretical_bankrupt(p, start, win_amount)`: Calculates theoretical ruin probability

## Dependencies

- `numpy`: Numerical computations
- `matplotlib`: Visualization

