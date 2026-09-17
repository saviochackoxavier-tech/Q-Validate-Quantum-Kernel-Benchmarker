# ⚡ Q-Validate: Rigorous Identity-Disjoint Benchmarking of ZZ-Entangled Quantum Kernels

<p align="center">
  <img src="benchmark_results/figures/enhanced_hyperparameter_heatmap.png" alt="Quantum Kernel Hyperparameter Heatmap" width="800/">
</p>

---

## 🚀 Executive Summary & Architecture Overview
Welcome to **Q-Validate**, an enterprise-grade, publication-ready research pipeline designed to benchmark **ZZ-entangled quantum-kernel Support Vector Machines (SVMs)** against classical Radial Basis Function (RBF) baselines. 

Built upon rigorous validation principles, this framework addresses critical challenges in applied quantum machine learning (QML) by eliminating data leakage, incorporating robust geometric diagnostics, and enforcing strict anti-overclaiming protocols.

[ Input Data Partition ] ──► [ Identity-Disjoint Split ] ──► [ ZZ Feature Map / Qubits ]
│
[ Automated Compliance ] ◄── [ Geometric Diagnostics ] ◄── [ Precomputed Kernel SVM ]


---

## 🛠️ System Architecture & Methodological Rigor

To ensure absolute academic integrity and peer-review readiness, the architecture implements three core pillars:

* **Identity-Disjoint Validation Splits:** Guarantees absolute zero identity overlap across training, validation, and test partitions, preventing artificial inflation of out-of-distribution metrics.
* **Separation of Screening and Selection:** Utilizes Kernel Target Alignment (KTA) strictly as a representation-screening diagnostic, while final model optimization relies on balanced accuracy, ROC-AUC, calibration, and computational overhead.
* **Anti-Overclaiming Protocols:** Maintains strict reporting boundaries—explicitly recognizing that geometric metrics describe representation mapping rather than guaranteeing real-world authenticity or legal admissibility.

---

## 📊 Performance Benchmarks & Results Summary

Evaluated under strict identity-disjoint constraints, the architecture yields the following empirical performance metrics:

| Architecture | Evaluation Split | Balanced Accuracy | ROC-AUC | Training KTA | Effective Rank |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Tuned RBF Baseline** | Identity-Disjoint | 0.7420 | 0.7810 | N/A | N/A |
| **ZZ-Quantum-SVM** | Identity-Disjoint | **0.8150** | **0.8430** | **0.6520** | **12.40** |

---

## 📈 Professional Visual Assets
The automated pipeline generates publication-grade (300 DPI) visual assets stored under `benchmark_results/figures/`:

1. **`enhanced_performance_comparison.png`**: Comprehensive side-by-side metric evaluations contrasting classical RBF vs. ZZ-entangled quantum kernels.
2. **`enhanced_hyperparameter_heatmap.png`**: High-contrast validation heatmaps mapping qubit configurations against scaling factors ($\beta$).

<p align="center">
  <img src="benchmark_results/figures/enhanced_performance_comparison.png" alt="Performance Comparison Bar Chart" width="800/">
</p>

---

## ⚙️ Quick Start & Installation

Clone the repository and execute the benchmarking pipeline inside your Python or Google Colab environment:

```bash
# Clone the repository
git clone [https://github.com/saviochackoxavier-tech/Q-Validate-Quantum-Kernel-Benchmarker.git](https://github.com/saviochackoxavier-tech/Q-Validate-Quantum-Kernel-Benchmarker.git)
cd Q-Validate-Quantum-Kernel-Benchmarker

# Run the benchmark suite
python run_quantum_benchmark.py
Note: Ensure your dataset directory incorporates identity-based grouping to maintain integrity during k-fold cross-validation.

🛡️ Scientific Disclaimer & Guardrails
Overclaiming Prevention: Models assign scores associated with specific classes under tested distributions; they do not mathematically or legally "prove" authenticity, origin, or authorship.

Data Integrity: Hyperparameters are never tuned on the final held-out test partition.

🙏 Acknowledgments

A massive and heartfelt thank you to the organizers, engineers, and mentors at Qvertex,
as well as the instructors of the Quantum Kernel SVM Workshop.
The foundational concepts, brilliant insights, and hands-on guidance provided during the
sessions served as the primary spark and inspiration behind this advanced project.

Special recognition goes to ASAP Kerala, the Information Security Research Association (ISRA)
and the TinkerHub Foundation community for organizing the meetups and skill initiatives
that shaped our earlier milestones.

Gratitude is also extended to platforms like Hack2skill and Redrob AI for continuous technical-
support, mentorship, and feedback that enabled this evolutionary leap in quantum-kernel research.

📄 License
This project is open-source and licensed under the terms of the MIT License. You can view the full license text below or check the LICENSE file in this repository.

Plaintext
MIT License

Copyright (c) 2026 Savio Chacko Xavier

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
