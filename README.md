# Safeguarding Networks from Malicious Intrusions using Quantum Machine Intelligence (QMGOA)

## 📌 Overview
This repository contains the implementation of **Quantum Multi-population Grasshopper Optimization Algorithm (QMGOA)** integrated with **Differential Evolution (DE)** for **feature selection** in **Intrusion Detection Systems (IDS)** within IoT environments.  
The project reproduces the work presented in the paper:

> **Shukla, A.K.** (2025). *Safeguarding Networks From Malicious Intrusions Using Quantum Machine Intelligence*. Software: Practice and Experience. DOI: [10.1002/spe.70004](https://doi.org/10.1002/spe.70004)

---

## 🎯 Motivation
The rapid expansion of IoT networks has created a larger attack surface for cyber threats such as DDoS, injection, impersonation, and flooding attacks.  
Conventional ML-based IDS approaches often:
- Struggle to adapt to dynamic environments.
- Have high **false positive rates (FPR)**.
- Fail to balance **exploration vs. exploitation** in feature selection.

**QMGOA** addresses these challenges by:
- Integrating **quantum computation concepts** (qubits, superposition, quantum rotation gates) with GOA.
- Employing a **multi-population strategy** to improve search diversity.
- Using **Differential Evolution (DE)** to refine solutions.
- Selecting optimal features for high-performance anomaly-based IDS.

---

## 🧠 Methodology

### 1. **Quantum-Enhanced Grasshopper Optimization**
- Uses quantum bits to represent features in superposition (`|0⟩` → selected, `|1⟩` → not selected).
- Enhances **exploration** and **exploitation** balance in search space.

### 2. **Multi-Population Strategy**
- Divides the population into subpopulations.
- Applies independent evolution with periodic migration for information sharing.

### 3. **Differential Evolution Refinement**
- Mutation, crossover, and selection operations improve local search.
- Prevents premature convergence.

### 4. **Feature Selection + Classification**
- SVM (Linear, Polynomial, RBF kernels) used to evaluate feature subsets.
- Best-performing kernel chosen for final IDS model.

---

## 📊 Datasets
The algorithm was evaluated on three benchmark IDS datasets:
- **NSL-KDD** — 41 features, improved version of KDD Cup 99 dataset.
- **UNSW-NB15** — 43 selected features capturing realistic attack scenarios.
- **BoT-IoT** — IoT-specific dataset with diverse network attack patterns.

- Whereas I've implemented it on UNSW-NB15, others are similar to work.

---

## 🚀 Results
Across all datasets, QMGOA consistently outperformed state-of-the-art metaheuristic optimizers (**GA, PSO, DE, CS, GOA**) in:
- **Accuracy**
- **Detection Rate (DR)**
- **Precision**
- **F-measure**
- **Reduced computation time**
