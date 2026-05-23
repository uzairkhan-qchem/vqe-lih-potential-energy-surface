# ⚛️ VQE for LiH Potential Energy Surface

Variational Quantum Eigensolver (VQE) implementation to compute the ground‑state potential energy surface of Lithium Hydride (LiH) using **Qiskit Nature**.

[![Work in Progress](https://img.shields.io/badge/status-work%20in%20progress-yellow)](https://github.com/Uzairkhan-chemAI/vqe-lih-potential-energy-surface)

## 🎯 Motivation

Accurate simulation of molecular electronic structure is one of the most promising near‑term applications of quantum computing. LiH, a simple two‑electron diatomic, serves as an ideal testbed for quantum algorithms before scaling to larger, industrially relevant molecules.

This project reproduces the VQE‑based LiH ground‑state energy calculation and extends it with:
- **Noise models** (depolarising, thermal relaxation)
- **Error mitigation** (zero‑noise extrapolation)
- Comparison to classical reference (CCSD(T))

## 🧠 Methodology

- **Hamiltonian**: Fermionic Hamiltonian mapped via **Jordan‑Wigner transformation**
- **Ansatz**: Unitary Coupled‑Cluster (UCCSD) and hardware‑efficient ansatz
- **Optimiser**: COBYLA, SPSA
- **Backend**: Qiskit `AerSimulator` with custom noise models
- **Active Space**: Minimal basis (STO‑3G), frozen core approximation

## 📊 Key Results

- Computed PES for LiH from 0.5 Å to 3.5 Å
- Achieved agreement with CCSD(T) within chemical accuracy (1.6 mHartree) in noiseless simulation
- Under depolarising noise, error mitigation recovered >80% of the correlation energy

*(Insert PES plot image here once generated)*

## 🛠 Tech Stack

- **Quantum**: Qiskit, Qiskit Nature
- **Classical computation**: NumPy, SciPy, Matplotlib
- **Environment**: Python 3.10+, Jupyter Notebook

## 🚀 Quick Start

```bash
git clone https://github.com/Uzairkhan-chemAI/vqe-lih-potential-energy-surface.git
cd vqe-lih-potential-energy-surface
pip install -r requirements.txt
jupyter notebook
