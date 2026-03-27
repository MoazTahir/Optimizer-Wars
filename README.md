# Optimizer Wars: A Scientific Investigation into Gradient Descent Optimizers

**Author:** Moaz Tahir | Student ID: 24178436  
**Course:** MSc Data Science — Machine Learning Tutorial Assignment  
**License:** MIT

---

## Overview

This tutorial compares five gradient descent optimizers: SGD, SGD with Momentum,
RMSProp, Adam, and AdamW, in a controlled experiment on the FashionMNIST dataset
using a fixed CNN architecture. Every optimizer receives the same model, the same
data, and the same learning rate. The only variable is the update rule.

The tutorial covers:
- Mathematical intuition behind each optimizer
- Convergence speed and learning rate sensitivity
- Loss landscape visualisation via PCA projection
- Decision boundary analysis on a spiral dataset
- A direct Adam vs AdamW overfitting experiment

---

## Repository Structure
```
optimizer-wars/
│
├── optimizer_wars_notebook.ipynb          # Main experiment notebook (all code + figures)
├── requirements.txt        # Python dependencies
├── report.pdf              # Tutorial report (<2000 words)
├── figures/                # All generated figures (auto-created by notebook)
└── README.md               # This file
```

---

## Getting Started

### 1. Clone the repository
```bash
git clone https://github.com/[YOUR_USERNAME]/optimizer-wars.git
cd optimizer-wars
```

### 2. Install dependencies

Python 3.9+ is recommended.
```bash
pip install -r requirements.txt
```

### 3. Run the notebook
```bash
jupyter notebook notebook.ipynb
```

Run all cells in order. The notebook will:
- Automatically download FashionMNIST (~30 MB) on first run
- Train all five optimizers sequentially
- Generate and save all figures to `./figures/`

**Expected runtime:** 10–20 minutes on CPU, 3–5 minutes on GPU.

---

## Requirements

See `requirements.txt`. Key dependencies:

| Package | Purpose |
|---|---|
| torch / torchvision | Model training and dataset |
| numpy / pandas | Numerical operations and results tables |
| matplotlib / seaborn | Static figures |
| plotly | Interactive 3D visualisations |
| scikit-learn | PCA for loss landscape projection |

---

## Reproducibility

All experiments use a fixed random seed (`SEED = 42`) applied to both PyTorch and
NumPy. All five optimizers are trained from identically initialised weights using
the same seed. Results should be fully reproducible across runs on the same hardware.
Minor numerical differences may occur between CPU and GPU due to floating-point
non-determinism in CUDA kernels.

---

## Accessibility

- All figures use the Wong (2011) colorblind-safe palette, verified safe for
  deuteranopia, protanopia, and tritanopia.
- Distinct line styles and markers are used in addition to color, so figures
  remain readable when printed in greyscale.
- Alt-text descriptions are provided for all figures in the PDF report.

---

## References

Full references are provided in the report and at the end of `notebook.ipynb`.
Key papers:

- Kingma & Ba (2015) — Adam: A Method for Stochastic Optimization. arXiv:1412.6980  
- Loshchilov & Hutter (2019) — Decoupled Weight Decay Regularization. arXiv:1711.05101  
- Ruder (2016) — An Overview of Gradient Descent Optimization Algorithms. arXiv:1609.04747  
- Li et al. (2018) — Visualizing the Loss Landscape of Neural Nets. arXiv:1712.09913

---

## License

This project is licensed under the MIT License. See below.
```
MIT License

Copyright (c) 2026 Moaz Tahir

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
permitted to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
```