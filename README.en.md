<p align="center">
  <a href="README.md">Русский</a> | <b>English</b> | <a href="README.de.md">Deutsch</a>
</p>

# Circular Waveguide Design (6.21 GHz)

This repository contains analytical calculations and 3D electromagnetic simulation results for a circular waveguide with a matching transition, designed to operate at **6.21 GHz**.

The project includes the calculation of the waveguide path geometry, selection of matching section dimensions, and performance verification of the structure using Finite-Difference Time-Domain (FDTD) analysis.

---

## Project Structure

* `/calculations` — analytical calculations of waveguide and matching transformer parameters in Mathcad format (`.xmcd`).
* `/simulation` — 3D electromagnetic simulation project in CST Studio Suite (`.cst`).
* `/docs/images` — graphical assets and result screenshots.

---

## Analytical Calculation

Analytical calculations of geometric and electrodynamic parameters (waveguide radius, cutoff wavelength for the dominant $H_{11}$ mode, wave impedance) were carried out in Mathcad. The baseline dimensions were determined considering frequency constraints to ensure single-mode operation.

### 1. Input Waveguide Calculation (400 Ohm)
Determining the baseline geometric dimensions to provide the required wave impedance at the operating frequency.
![Input waveguide calculation](docs/images/calc_waveguide_400_ohm.png)

### 2. Matching Section Calculation
Calculating the parameters of a quarter-wave transformer to minimize reflections at the junction of the two sections.
![Matching section calculation](docs/images/calc_matching_transformer.png)

### 3. Output Waveguide Calculation (800 Ohm)
Calculating the geometry of the waveguide with increased wave impedance.
![Output waveguide calculation](docs/images/calc_waveguide_800_ohm.jpg)

---

## 3D Numerical Simulation

Based on the analytical calculations, a 3D model of a circular waveguide with a bend and a matching transition was built in CST Studio Suite.

![3D Waveguide Model](docs/images/simulation_3d_model.png)

### Z-Parameter Analysis Results

The plot of the input impedance magnitude ($Z_{1,1}$) validates the calculated parameters at the operating frequency:
* **Operating Frequency:** 6.2106 GHz
* **Input Impedance ($Z_{1,1}$):** ~485 Ohm
* **VSWR:** ~1.2

![Z-parameters plot](docs/images/simulation_z_parameters.png)

## License

Copyright (c) 2026 Ilya Kornilov

This source document describes open hardware and is licensed under the CERN-OHL-P v2 license.
You may redistribute and modify this source document, and make products using it, under the terms of the CERN-OHL-P v2 (https://cern.ch/cern-ohl).

This source document is distributed WITHOUT ANY EXPRESS OR IMPLIED WARRANTY, INCLUDING OF MERCHANTABILITY, SATISFACTORY QUALITY OR FITNESS FOR A PARTICULAR PURPOSE. Please see the CERN-OHL-P v2 for applicable conditions.
