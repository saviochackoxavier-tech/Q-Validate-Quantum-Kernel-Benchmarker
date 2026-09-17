# ⚡ Q-Validate: Rigorous Identity-Disjoint Benchmarking of ZZ-Entangled Quantum Kernels

<p align="center">
  <img src="figures/synthetic_pipeline_demo_1.png" alt="Quantum Kernel Hyperparameter Heatmap" width="800/">
</p>

<p align="center">
  <em>An enterprise-grade, publication-ready research framework engineering robust evaluations of ZZ-entangled quantum-kernel SVMs against classical RBF baselines with absolute data-leakage immunity.</em>
</p>

---

## 🚀 Executive Summary & Architecture Overview

Welcome to **Q-Validate**, a state-of-the-art research framework engineered to conquer fundamental evaluation bottlenecks in Applied Quantum Machine Learning (QML). Traditional deepfake detection and biometric identification pipelines frequently succumb to severe cross-validation vulnerabilities—specifically data leakage via random splits where frames belonging to the exact same subject bleed across training and testing partitions. 

This repository enforces strict **identity-disjoint data splitting**, integrates advanced geometric diagnostics including **Kernel Target Alignment (KTA)** and **Effective Rank**, and executes clean, reproducible comparative performance pipelines between classical Support Vector Machines and **ZZ-entangled quantum-kernel SVMs**.

[ FaceForensics++ Raw Data ]
│
▼
[ src/extract_arcface_embeddings_colab.py ] ──► Extracts Embeddings & Metadata (identity_id)
│
▼
[ src/run_faceforensics_quantum_benchmark.py ] ──► Identity-Disjoint Split & ZZ-Kernel Evaluation
│
▼
[ src/benchmark_results_to_latex.py ] ──► Compiles Publication-Ready LaTeX Tables


---

## 📂 Repository Structure

The project is structured cleanly to isolate pre-flight simulation smoke tests from production datasets and core execution engines:

```text
quantum-kernel-svm-benchmark/
├── notebooks/
│   └── Q_Validate_Rigorous_Identity_Disjoint_Benchmarking_of_ZZ_Entangled_Quantum_Kernels.ipynb
├── figures/
│   ├── synthetic_pipeline_demo_1.png
│   ├── synthetic_pipeline_demo_2.png
│   └── README.md
├── src/
│   ├── extract_arcface_embeddings_colab.py
│   ├── run_faceforensics_quantum_benchmark.py
│   └── benchmark_results_to_latex.py
├── results/
│   └── README.md
├── LICENSE
└── README.md
🛠️ Detailed Component Guide & Execution Workflow
To replicate the empirical benchmarking suite or scale the architecture using real-world data files, execute the three core python scripts in sequence:

1. Feature Extraction (src/extract_arcface_embeddings_colab.py)
Processes raw video frames or image crops to extract high-dimensional facial feature tensors via ArcFace. It extracts and bundles necessary metadata tags—including identity_id, video_id, and manipulation class targets—to power subject-exclusive partitioning.

Usage Example:

Bash
python src/extract_arcface_embeddings_colab.py --data_dir /path/to/faceforensics --output_dir results/
2. Empirical Benchmarking (src/run_faceforensics_quantum_benchmark.py)
The heavy-lifting execution core of the repository. It ingests stored embedding arrays, runs a strict subject-exclusive (identity-disjoint) split, constructs the parameterized ZZ-entangled quantum kernel matrix, fits the quantum-kernel SVM, and computes critical geometric diagnostics such as Kernel Target Alignment (KTA) and effective rank.

Usage Example:

Bash
python src/run_faceforensics_quantum_benchmark.py --input_embeddings results/embeddings.npz --qubits 8 --gamma 0.05
3. LaTeX Table Generation (src/benchmark_results_to_latex.py)
Automates paper drafting by parsing experimental metric JSON logs and compiling them into pristine, publication-ready LaTeX table code optimized for direct insertion into academic manuscripts.

Usage Example:

Bash
python src/benchmark_results_to_latex.py --results_json results/metrics.json --output_tex results/performance_table.tex
⚠️ Important Note on Artifacts & Synthetic Demos
The visual assets saved inside the figures/ directory and the core notebook (Q_Validate_Rigorous_Identity_Disjoint_Benchmarking_of_ZZ_Entangled_Quantum_Kernels.ipynb) serve as synthetic pipeline smoke tests and presentation prototypes.

They demonstrate the planned data schema validation, visualization grid layout, and metric export flow using simulated random features and hard-coded mathematical fallback routines.

They do not represent lawful FaceForensics++ empirical results, nor do they substantiate claims of quantum advantage or production deepfake-authentication performance until re-executed with genuine dataset embeddings.

Figure Caption Policy: Synthetic pre-flight visualization generated during pipeline validation; not a FaceForensics++ result.

⚙️ Quick Start & Environment Setup
Get your environment configured in minutes:

Bash
# 1. Clone the repository
git clone [https://github.com/saviochackoxavier-tech/Q-Validate-Quantum-Kernel-Benchmarker.git](https://github.com/saviochackoxavier-tech/Q-Validate-Quantum-Kernel-Benchmarker.git)
cd Q-Validate-Quantum-Kernel-Benchmarker

# 2. Create and activate a Python virtual environment
python -m venv venv
source venv/bin/activate  # On Windows use: venv\Scripts\activate

# 3. Install core dependencies
pip install numpy scipy scikit-learn matplotlib jupyter pennylane

🙏 Acknowledgments & Professional Context

This framework draws direct inspiration from applied research initiatives
in infrastructure security, quantum computing workshops,
and deep learning engineering communities.

A massive thank you to the organizers, engineers,
and mentors at Qvertex, as well as the instructors
of the Quantum Kernel SVM Workshop.

Special recognition goes to collaborative technical meetups
hosted by organizations like the Information Security Research Association (ISRA)
and the TinkerHub Foundation, alongside skill development milestones
via ASAP Kerala and hackathon platforms like Hack2skill
and Redrob AI for continuous technical support,
community feedback, and shaping our technical foundations.

📄 MIT License
Copyright (c) 2026 Savio Chacko Xavier

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
