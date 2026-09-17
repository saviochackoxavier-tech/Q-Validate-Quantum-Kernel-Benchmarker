# Audit of `Q_Validate_Rigorous_Identity_Disjoint_Benchmarking_of_ZZ_Entangled_Quantum_Kernels.ipynb`

## Bottom-line assessment

The notebook is sufficient as a **pipeline smoke test and presentation prototype**. It is not sufficient as the empirical basis for the article’s FaceForensics++ claims. Its current outputs should not be described as FaceForensics++ results, quantum-kernel results, or rigorous identity-disjoint benchmark results.

## What the notebook actually demonstrates

The notebook installs common dependencies, creates a synthetic feature bundle with `X`, `y`, `identity_id`, and `video_id`, runs one classical RBF SVM on four selected random features, creates a CSV, generates a simulated hyperparameter table, and exports two embedded figures.

The reported synthetic RBF metrics are:

| Metric | Notebook output |
|---|---:|
| Accuracy | 0.5667 |
| Precision | 0.6000 |
| Recall | 0.7500 |
| F1 score | 0.6667 |

These values are valid only as outputs of the notebook’s synthetic smoke test. They are not evidence about FaceForensics++ or ArcFace embeddings.

## Issues to correct before article use

1. **Random labels.** The synthetic labels are generated independently with `np.random.randint(0, 2, ...)`. They do not represent a meaningful nonlinear manifold or a deepfake-generation process.
2. **No identity-disjoint split.** The notebook creates `identity_id`, but the benchmark uses ordinary `train_test_split` without groups. The identity metadata is therefore not used to prevent leakage.
3. **No quantum-kernel model.** The main benchmark cell runs only an RBF SVM. It does not construct a `QuantumCircuit`, compute statevectors, build a quantum kernel, or train a precomputed-kernel SVM.
4. **Simulated tuning results.** The hyperparameter cell calculates `simulated_score` from a formula. These values are not measured validation results.
5. **Hard-coded fallback metrics.** The final graph/reporting cell uses fallback values when expected columns are absent, including values for quantum accuracy, ROC-AUC, KTA, and effective rank. Those values must not appear in the article.
6. **Example baseline values in a graph.** The plotted RBF comparison includes manually supplied values `[0.74, 0.76, 0.73, 0.74]`. These are illustrative, not measured.
7. **No KTA or effective-rank calculation.** The notebook does not compute the mathematical diagnostics defined in the manuscript.
8. **No calibration, PR-AUC, specificity, confidence intervals, or robustness testing.** The article requires these for a defensible empirical section.
9. **No FaceForensics++ data.** The notebook does not load lawful FaceForensics++ crops or embeddings.

## What can be retained

The notebook can be retained as a preliminary Colab pipeline check. Its `.npz` schema is directionally correct, and the output directory structure can be reused. The image assets can be placed in a GitHub repository only if they are captioned as **synthetic pre-flight demonstrations** and not as FaceForensics++ findings.

## Required next run for the article

Use the ArcFace extraction script to create a lawful embedding NPZ with `X`, `y`, `identity_id`, `video_id`, `manipulation`, and `path`. Then run the identity-disjoint quantum benchmark and replace the synthetic notebook’s main benchmark, simulated tuning, and fallback graph cells with measured outputs. Only those measured outputs should populate the manuscript tables and figures.

## Recommended GitHub wording

> The included figures are generated from a synthetic pipeline smoke test. They demonstrate the planned visualisation and export workflow; they are not FaceForensics++ results and do not establish quantum advantage or deepfake-authentication performance.
