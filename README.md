# Free-Space QKD Under Atmospheric Fluctuations

This repository contains Python simulations and Jupyter Notebooks developed for my Master's thesis on **Free-Space Quantum Key Distribution (QKD)**. Check the full thesis [here](https://gehadibany.github.io/files/Thesis.pdf) for context.

The project models a satellite-to-ground QKD downlink and connects a turbulence-informed model to the secure key rate (SKR) and quantum bit error rate (QBER). Mitigation strategies (optimised operating parameters) were proposed based on the results.

### Key Features and Physics Models
* **Atmospheric Modeling:** Implements the **Kim model** for visibility and attenuation.
* **Turbulence Profile:** Hufnagel-Valley / Stotts model for the refractive index structure parameter ($C_n^2$) to account for altitude dependence.
* **Coupling Efficiency:** Models based on the Strehl ratio and Fried parameter.
* **Turbulence Effects:** Simulates beam spreading, scintillation (Rytov variance), and beam wander.
* **Performance Metrics:** Calculates Total Efficiency ($\eta_{tot}$), QBER, and Secret Key Rate (SKR).
* **Optimization:** Analyzes trade-offs between signal collection and background noise to find optimal receiver aperture sizes.



## Repository Structure

The analysis is divided into four main notebooks:
### 1. `operational_parameters_selection.ipynb`
Performs a parameter sweep to determine the best configuration for the link based on the tested variables and the outputs.

### 2. `beam_wander_simulation.ipynb`
A Monte Carlo simulation to show how turbulence causes the beam centroid to drift at the receiver's focal plane.

### 3. `aperture_radius_optimisation.ipynb`
To analyze the trade-off between light collection efficiency, background noise and coupling.

### 4. `mitigations_effects_QBER.ipynb`
The final analysis comparing the system performance before and after optimization (selection of parameters based on the results of the above analyses)

## Requirements

* Python 3.x
* `numpy`
* `scipy`
* `matplotlib`