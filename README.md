# 🧠 SVM Optimization Experiment

## 📌 Overview
This repository presents an **SVM optimization experiment** for **multi-class classification** using synthetic data. The goal is to evaluate and compare SVM performance with different kernels and hyperparameters to identify the best configuration.

---

## 🚀 Features
- 🧪 Synthetic dataset with **5000 samples** and **10 features**
- 🔍 Hyperparameter tuning for:
  - Linear kernel
  - RBF kernel
  - Polynomial kernel
- 🔁 Evaluation across **10 different train/test splits**
- 📊 Visualizations:
  - Convergence curves
  - Class distribution
  - Feature correlations
- 📁 Exportable results and graphs for GitHub showcasing

---

## 📂 Dataset
- **Samples**: 5000  
- **Features**: 10 (7 informative, 3 redundant)  
- **Classes**: 5 (balanced distribution)  
- **Preprocessing**: Standardization using `StandardScaler`

---

## ⚙️ Methodology

1. Generate synthetic classification dataset via `make_classification`
2. Preprocess: scaling + class balance verification
3. Create **10 different train/test splits** (70/30 ratio)
4. Optimize SVM using grid search:
   - **Linear**: C values
   - **RBF**: C and gamma
   - **Polynomial**: C and degree
5. Track model convergence (accuracy vs iterations)
6. Store and visualize results

---

## 📈 Results Summary

| Sample | Best Accuracy | Best SVM Parameters       |
|--------|----------------|---------------------------|
| S1     | 0.982          | Linear, C=0.464           |
| S2     | 0.971          | RBF, C=2.154, γ=0.005     |
| S3     | 0.994          | Linear, C=0.1             |
| S4     | 0.988          | Linear, C=2.154           |
| S5     | 0.994          | RBF, C=2.154, γ=0.005     |
| S6     | 0.988          | Linear, C=0.022           |
| S7     | 0.982          | RBF, C=215.443, γ=0.001   |
| S8     | 0.982          | Linear, C=0.464           |
| S9     | 0.988          | Poly, C=0.022, degree=3   |
| S10    | 0.994          | Linear, C=2.154           |

> 🔥 **Highest Accuracy**: 0.994 (Samples S3, S5, S10)

---

## 📝 Output Files

- `results.csv`: Accuracy and parameters per sample
- `.png` plots: for convergence, class balance, and correlation
- Use in GitHub documentation or reports

---

## 📦 Dependencies

```text
Python 3.x  
numpy  
pandas  
scikit-learn  
matplotlib  
seaborn
```

Install using:

```bash
pip install -r requirements.txt
```

---

## ▶️ Usage

### Clone and Run

```bash
git clone https://github.com/varunkumar2004/parameter-optimisation-using-support-vector-machine.git
```

## 🤝 Contributing

Contributions are welcome! Feel free to fork the repository, suggest improvements, and submit pull requests.
