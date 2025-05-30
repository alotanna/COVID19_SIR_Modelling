# COVID-19 Disease Spread Simulation

A Python implementation of mathematical models to simulate COVID-19 epidemic dynamics and analyze intervention strategies.

## Overview

This project uses non-linear modeling approaches to understand disease progression and evaluate the effectiveness of different public health interventions. The simulation helps analyze how lockdowns and vaccination campaigns impact epidemic spread patterns.

## Mathematical Models

### SIR Model
The primary model divides the population into three compartments:
- **S**: Susceptible individuals who can be infected
- **I**: Infected individuals who can transmit the disease
- **R**: Recovered/Removed individuals (immune or deceased)

**Differential Equations:**
```
dS/dt = -β(SI/N)
dI/dt = β(SI/N) - γI
dR/dt = γI
```

**Key Parameters:**
- `β`: Transmission rate (higher values = faster spread)
- `γ`: Recovery rate (1/γ = average infectious period)
- `R₀`: Basic reproduction number (β/γ)
- `N`: Total population size

### Logistic Growth Model
Initial approach for understanding epidemic progression:
```
dN/dt = rN(1 - N/K)
```
Where `N` is infected population, `r` is growth rate, and `K` is carrying capacity.

## Intervention Strategies

### Lockdown Interventions
- **Mechanism**: Reduces transmission rate (β)
- **Variables**: Different reduction percentages and implementation timings
- **Analysis**: Effectiveness vs. timing (days 100-1000)

### Vaccination Interventions
- **Mechanism**: Increases recovery rate (γ)
- **Variables**: Different vaccination speeds and campaign start times
- **Focus**: Long-term population immunity effects

## Key Features

- Simulate epidemic progression over time
- Compare different intervention strategies
- Analyze timing effects (early vs. delayed interventions)
- Generate epidemic curves and visualizations
- Test various parameter combinations

## Results Summary

**Lockdown Findings:**
- More effective lockdowns (higher β reduction) → lower peak infections
- Earlier implementation → significantly better outcomes
- Temporary effects requiring sustained measures

**Vaccination Findings:**
- Higher vaccination rates → faster epidemic resolution
- Early campaigns → more effective long-term control
- More durable protection compared to lockdowns

**Key Insight:** Combined approaches provide the most robust epidemic control.

## Usage

The code includes simulation scripts for:
1. Basic SIR model runs
2. Intervention scenario comparisons
3. Parameter sensitivity analysis
4. Visualization of results

Run the main simulation files to generate epidemic curves and analyze different intervention scenarios.

## Model Assumptions

- Homogeneous population mixing
- Fixed infection and recovery rates
- No reinfections (permanent immunity)
- No demographic changes during simulation period

---

*Course Project: Introduction to Modelling and Simulation*  
*Team: Ama Annor, Austine Iheji, Edward Mensah, Eric Hantungimana, Susanna Agyapong*  
*April 2025*