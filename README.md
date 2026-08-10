# Kerja Praktik (Internship) BRIN: Quantum Battery Simulation

**Author:** Umar Zaki Gunawan (Telkom University)  
**Institution:** Badan Riset dan Inovasi Nasional (BRIN)  

---

## 📌 Project Overview

This repository contains the source code, generated data, and reports for an internship project conducted at **BRIN (Badan Riset dan Inovasi Nasional)**. 

The main objective of this project is to simulate the dissipative dynamics of a quantum battery and reproduce the findings (specifically Figure 3c) from the paper:
> **"Superextensive electrical power from a quantum battery"**  
> *Hymas et al., Light: Science & Applications 15, 168 (2026)*

The simulations model a driven Tavis-Cummings Hamiltonian for an ensemble of four-level CuPc molecules coupled to a single cavity mode. The system's dynamics are evaluated by solving the Lindblad master equation using the **QuTiP (Quantum Toolbox in Python)** library. The models account for:
- Cavity losses ($\kappa$)
- Singlet non-radiative decay ($\gamma^-$)
- Triplet decay ($\gamma_T^-$)
- Singlet dephasing ($\gamma^z$)
- Intersystem crossing ($\gamma_{ISC}$)

## 📁 Repository Structure

- **`Source Code/`**  
  Contains Jupyter Notebooks for various simulation conditions:
  - `super-qb-baseline.ipynb` - Baseline simulation reproducing the main results.
  - `dissipative_dynamics.ipynb` - General dissipative dynamics solver (various conditions, e.g., $\kappa=0, \gamma=0$).
  - `super-qb-noym.ipynb` - Simulation without specific decay/coupling terms.
  - `super-qb-noyt.ipynb` - Simulation without specific triplet decay/coupling terms.
  - `super-qb-noymyt.ipynb` - Simulation omitting multiple specific terms.
  
- **`Data/`**  
  Contains the output simulation data in both `.csv` and `.npz` formats, such as:
  - Stored energy and charging power data (`energy_power_*.csv`, `fig3c_energy_power.*`)
  - Population state resolutions over time (`population-res-*.csv`)
  - QuTiP expectation values (`fig3c_qutip_data.csv`)

- **`Laporan-KP-BRIN-Umar-Zaki-Gunawan-(BAB.3-4).pdf`**  
  The formal Internship Report (Laporan Kerja Praktik), covering Chapters 3 and 4, detailing the methodology, simulation setups, and results.

- **`presentasi.pdf`**  
  The presentation slides summarizing the project, results, and conclusions.

## 🛠️ Prerequisites & Installation

To run the simulation notebooks, you need a Python environment with the following libraries installed:
- `python >= 3.8`
- `qutip`
- `numpy`
- `matplotlib`
- `scipy`
- `jupyter`

You can install the dependencies via pip:
```bash
pip install qutip numpy matplotlib scipy jupyter
```

## 🚀 Usage

1. Clone this repository to your local machine.
2. Navigate to the `Source Code` directory.
3. Launch Jupyter Notebook or Jupyter Lab:
   ```bash
   jupyter notebook
   ```
4. Open any of the `.ipynb` files (e.g., `super-qb-baseline.ipynb`) and run the cells sequentially to perform the simulations and plot the graphs.

## 📊 Results

The primary output of the simulation is the time-evolution of the molecular states ($S_1^0, S_1^1, T_1$), charging power, and stored energy in the quantum battery model. The generated plots will automatically match the theoretical results (such as Fig 3c) from the reference paper, highlighting the behavior of the system under ultrafast laser excitation.

---
*This repository is a result of a Kerja Praktik (Internship) program at BRIN. All codes are provided for academic and reproduction purposes.*
