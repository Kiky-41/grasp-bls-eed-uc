# 🌿 GRASP-BLS for Economic Emission Dispatch with Unit Commitment
[![DOI](https://zenodo.org/badge/1205023389.svg)](https://doi.org/10.5281/zenodo.19472870)

Hybrid optimization framework combining **GRASP (Greedy Randomized Adaptive Search Procedure)** and **Backtracking Line Search (BLS)** for solving the **Economic Emission Dispatch (EED)** problem with Unit Commitment in power systems.

This project demonstrates how a hybrid metaheuristic and gradient-based approach can simultaneously minimize fuel cost and emission in generator scheduling.

---

## 📄 Related Publication

Raharjo, J., Ikhsan, R.R.N., Yustika, L.M. (2025)
*A Greedy Adaptive and Backtracking Framework for Reducing Emission Costs in Generator Scheduling*
International Journal of Technology
https://doi.org/10.14716/ijtech.v16i6.7588

---

## 🚀 Features

- 🌿 Hybrid metaheuristic + gradient-based optimization (**GRASP + BLS**)
- 🎯 Multi-objective: **fuel cost minimization** and **emission reduction**
- ⚙️ Supports key constraints:
  - Power balance constraint
  - Generator limits
  - Ramp rate constraints
- 🔁 Supports **Unit Commitment** (generator ON/OFF scheduling)
- 📅 Works on **dynamic 24-hour load scenarios**
- 🧠 Clean and modular Python implementation

---

## 🧠 Method Overview

The EED problem aims to minimize two objectives simultaneously:

**1. Fuel Cost:**

$$F(P) = \sum_{i=1}^{n} (a_i P_i^2 + b_i P_i + c_i)$$

**2. Emission:**

$$E(P) = \sum_{i=1}^{n} (d_i P_i^2 + e_i P_i + f_i)$$

The hybrid framework operates in two phases:

- **GRASP** → global exploration with diverse candidate solutions, avoids local optima
- **BLS** → local refinement using gradient-based line search near the optimal region

This approach ensures strong convergence, stability, and full constraint satisfaction.

---

## 📊 Key Results

| Metric | Value |
|--------|-------|
| Cost reduction vs Simulated Annealing | ~0.4% |
| Emission reduction | up to 22.25% |
| Cost improvement vs GSA, GWO, PSO | 5–9% |
| Power balance satisfied | ✅ |
| Ramp rate respected | ✅ |
| Generator limits enforced | ✅ |

**GRASP-BLS achieves:**
- Competitive cost and emission performance
- Full constraint satisfaction across all scenarios
- Robust convergence on dynamic load profiles

---

## 📂 Project Structure

```text
grasp-bls-eed-uc/
├── GRASP-BLS (EED-UC).ipynb   # Main implementation
├── dataset/                    # Input data
├── results/                    # Output & analysis
└── README.md
```

---

## ⚙️ Requirements

- Python 3.x
- NumPy
- Matplotlib
- Jupyter Notebook

Install dependencies:

```bash
pip install numpy matplotlib
```

---

## ▶️ Usage

Clone and run the notebook:

```bash
git clone https://github.com/Kiky-41/grasp-bls-eed-uc.git
cd grasp-bls-eed-uc
jupyter notebook
```

Open `GRASP-BLS (EED-UC).ipynb` and run all cells.

---

## 📊 Dataset

> ⚠️ The dataset used in the original research is not publicly available due to confidentiality restrictions.

You can:
- Use your own dataset with the same format
- Generate synthetic data for testing

**Expected Input Format**

| Parameter | Description |
|-----------|-------------|
| a, b, c   | Cost coefficients |
| Pmin      | Minimum power output |
| Pmax      | Maximum power output |
| RampUp    | Ramp up limit |
| RampDown  | Ramp down limit |

---

## 📌 Reproducibility

This repository focuses on the algorithm implementation.
Exact reproduction of published results requires proprietary datasets.

---

## 📖 Citation

If you use this work, please cite:

```bibtex
@article{raharjo2025graspbls,
  title={A Greedy Adaptive and Backtracking Framework for Reducing Emission Costs in Generator Scheduling},
  author={Raharjo, Jangkung and Ikhsan, Rifki Rahman Nur and Yustika, Lindiasari Martha},
  journal={International Journal of Technology},
  year={2025},
  doi={10.14716/ijtech.v16i6.7588}
}
```

---

## 🔗 DOI (Zenodo)

After creating a GitHub release, Zenodo will automatically generate a DOI for this repository.

---

## 📜 License

Creative Commons Attribution 4.0 International (CC BY 4.0)

---

## 🙌 Acknowledgements

This work is based on research in power system optimization, economic emission dispatch, and hybrid metaheuristic methods.

---

## ⭐ Support

If you find this repository useful:
- ⭐ Star this repo
- 🍴 Fork and contribute
- 📢 Share with the research community
