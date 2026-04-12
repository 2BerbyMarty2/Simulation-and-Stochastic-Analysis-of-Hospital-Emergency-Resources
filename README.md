# ER-Resource-Simulation: Stochastic Analysis of Staffing Levels

## About
A **Discrete-Event Simulation (DES)** built in **R** using the `simmer` package to evaluate hospital Emergency Room (ER) efficiency. This project models the stochastic nature of patient flows to determine if current staffing levels meet safety mandates.

## Key Features
* **Stochastic Modeling:** Implements **Poisson arrival processes** and **Exponential service time distributions**.
* **Resource Optimization:** Compares multi-server configurations (3 vs. 4 triage doctors).
* **Performance Metrics:** Tracks average waiting times, queue lengths, and resource utilization for 500+ patients.
* **Reproducibility:** Uses `set.seed` to ensure simulation consistency across environments (Colab/RStudio).

## Mathematical Framework
The simulation is based on an **M/M/c queuing model**, where:
* **Arrival Rate ($\lambda$):** 12 patients/hour (0.2 patients/min).
* **Service Rate ($\mu$):** 1/12 patients/min (12-minute average treatment).
* **Safety Threshold:** Average waiting time must remain $< 10$ minutes.



## Getting Started
### Prerequisites
Ensure you have the following R packages installed:
```r
install.packages(c("simmer", "simmer.plot", "tidyverse", "gridExtra"))
```

### Usage
1.  Open the `.Rmd` file in RStudio or Google Colab (R Runtime).
2.  Run the simulation chunks to generate performance data.
3.  Knit the file to PDF to view the full stochastic analysis and visualizations.
