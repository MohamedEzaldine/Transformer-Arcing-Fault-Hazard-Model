# Transformer Oil-Spill Hazard Simulator (Module 2)

A Python GUI application to evaluate the physical risks of internal arcing faults in oil-filled distribution transformers. It estimates tank overpressure, oil spill distance, and safe clearances. This tool represents Module 2 of the CIRED "Proximity of Urban Networks" project.

---

## Features

*   **Arc Energy Calculation:** Computes energy using physical voltage gradients.
*   **Pressure Estimation:** Calibrated model to find peak dynamic tank pressure.
*   **Current Bounding:** Limits fault currents based on IEC 60076-5 impedance or network capacity.
*   **Spill Distance:** Calculates oil ejection using Torricelli’s law and ballistic physics.
*   **Interactive UI:** Built with Tkinter, featuring a live hazard map and risk scores.
*   **Calibration Script:** Adjusts model parameters using experimental data.

---

## Core Equations

**1. Arc Energy Generation**
`E_arc = W * (G_arc * L_gap) * I_eff * t`

**2. Peak Tank Overpressure**
`Δp = A_E * (E_arc / V_oil)`

**3. Oil Spill Distance**
`v_eject = C_d * √(2 * Δp_eject / ρ_oil)`

`R = η * (v_eject² / g)`

## Repository Structure

*   `transformer_hazard_simulator.py`: Main dashboard and core simulator engine.
*   `calibration_harness.py`: Optimization module to regress physical parameters against test data.
*   `requirements.txt`: Required Python dependencies.
*   `.gitignore`: Git ignore rules.

---
<img width="1915" height="1023" alt="2" src="https://github.com/user-attachments/assets/e892c3af-373e-4b17-a486-5d09aa0f2370" />

## Getting Started

**1. Install dependencies:**
```bash
pip install -r requirements.txt
