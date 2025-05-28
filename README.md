# Steak Heat Transfer Simulation

## Project Overview

This project models the cooking of a steak using the **one-dimensional heat equation**, a partial differential equation (PDE) that simulates heat conduction. We implemented a **finite difference method (FDM)** in Python to simulate how temperature diffuses through the steak during grilling. The model includes **realistic flipping behavior**, where the steak is turned halfway through the cooking process to simulate bilateral heating.

## Purpose

The project aims to:
- Predict how heat transfers through a steak over time.
- Estimate cooking times for various doneness levels (rare, medium, well-done, etc.).
- Provide a mathematical and computational framework for robotic or automated cooking applications.

---

## Key Concepts

- **Heat Equation (PDE)**: `∂u/∂t = κ ∂²u/∂z²`
- **Boundary Conditions**:
  - Dirichlet at bottom (grill): Fixed at 450°F.
  - Neumann at top: Insulated or flipped at midpoint.
- **Initial Conditions**: Room temperature (70°F) throughout.
- **Flipping Logic**: Boundary conditions switch at t = 240s.
- **Numerical Method**: Explicit finite difference scheme.
- **Thermal Diffusivity**: κ = 0.00133 cm²/s

---

## Results Summary

- Flipping the steak after ~240s led to more even cooking and faster core temperature rise.
- Estimated cooking times for various doneness levels (Rare to Well Done) closely matched real-world grilling guides.
- Without flipping, heat accumulates unevenly, causing potential overcooking on one side.

---

## Files

```plaintext
steak_simulation_analysis.ipynb   # Jupyter notebook with full model, simulation, and plots
Steak Heat Transfer Modelling Project Report.pdf   # Full write-up of methods, results, and validation
README.md                         # You're here
```

---

## Dependencies

- Python 3.x
- `numpy`
- `matplotlib`
- `pandas`
- `seaborn` (optional, for enhanced plots)

Install with:

```bash
pip install numpy matplotlib pandas seaborn
```

---

## Future Work

- Incorporate **2D/3D heat transfer** for thicker or irregular cuts.
- Add **moisture loss**, **Maillard reactions**, and **protein denaturation** to simulate more realistic cooking.
- Validate against real thermocouple data from cooking experiments.