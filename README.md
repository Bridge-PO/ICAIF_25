# Bridging Prediction and Optimization: Decision-Focused Learning in Financial Optimization
<div align="center">
  <img src="assets/logo-website-style.svg" alt="DFL Logo" width="800"/>
  <br/>
  <br/>

# Decision-Focused Learning in Financial Optimization

[![ICAIF 2025](https://img.shields.io/badge/ICAIF-2025-red)](https://icaif25.org/)
[![Tutorial](https://img.shields.io/badge/Tutorial-November%2015-blue)](https://bridge-po.github.io/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

**Official repository for the Decision-Focused Learning tutorial at [ICAIF 2025](https://icaif25.org/)**

[🌐 Website](https://bridge-po.github.io/) • [📖 Documentation](#) • [💻 Notebooks](#notebooks) • [👥 Organizers](#organizers)

</div>

---

## 📋 Overview

This tutorial introduces **Decision-Focused Learning (DFL)** and its applications to financial optimization problems. Unlike traditional prediction-focused approaches, DFL directly aligns machine learning training objectives with the quality of downstream decisions, leading to superior performance in portfolio optimization and financial decision-making tasks.

**📅 Date:** Saturday, November 15, 2025  
**⏰ Time:** 2:00 PM - 5:30 PM SGT  
**📍 Location:** Singapore  
**🎯 Duration:** 3.5 hours  

## 🎓 What You'll Learn

- Fundamental differences between Prediction-Focused Learning (PFL) and Decision-Focused Learning (DFL)
- How to implement end-to-end differentiable optimization with PyTorch and cvxpylayers
- Applications of DFL to Mean-Variance Optimization and Portfolio Management
- Techniques for partial index tracking with DFL
- Practical hands-on experience with real financial datasets

## 📚 Tutorial Schedule

| Session | Title | Speaker | Duration |
|---------|-------|---------|----------|
| **1** | Introduction & Motivation | Yongjae Lee (UNIST) | 20 min |
| **2** | Background in Decision-Focused Learning | Haeun Jeon (KAIST) | 30 min |
| **3** | DFL in Mean-Variance Optimization | Junhyeong Lee (UNIST) | 30 min |
| **4** | DFL in Partial Index Tracking | Hyunglip Bae (KAIST) | 30 min |
| **5** | Closing Remarks & Future Directions | Yongjae Lee (UNIST) | 10 min |

### Session 1: Introduction & Motivation
- Overview of DFL vs. PFL paradigms
- Motivation in financial applications
- Why prediction accuracy ≠ better decisions

### Session 2: Background in Decision-Focused Learning
- PFL vs DFL pipeline comparison
- Theoretical considerations and challenges
- **[Hands-on Exercise]** Building a simple DFL model with PyTorch

### Session 3: DFL in Mean-Variance Optimization
- Markowitz framework review
- **[Hands-on Exercise]** Complete DFL pipeline implementation
- PFL vs DFL performance comparison with real market data

### Session 4: DFL in Partial Index Tracking
- Partial index tracking problem formulation
- Semi-definite relaxation techniques
- **[Hands-on Exercise]** DFL for partial index tracking with CvxpyLayer

### Session 5: Closing Remarks & Future Directions
- Open research challenges
- Q&A with all organizers

## 🛠️ Prerequisites

- **Programming:** Python 3.8+
- **Knowledge:**
  - Basic machine learning concepts
  - Familiarity with PyTorch
  - Optimization theory (helpful but not required)

## 📦 Installation

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/dfl-icaif2025.git
cd dfl-icaif2025
```

### 2. Create a Virtual Environment
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

### Required Packages
```
torch>=2.0.0
cvxpy>=1.4.0
cvxpylayers>=0.1.6
numpy>=1.24.0
pandas>=2.0.0
matplotlib>=3.7.0
jupyter>=1.0.0
yfinance>=0.2.0
```

## 🚀 Quick Start

### Running the Notebooks

Navigate to the `notebooks/` directory and start Jupyter:

```bash
cd notebooks
jupyter notebook
```

The tutorial notebooks are organized as follows:

```
notebooks/
├── 01_introduction_to_dfl.ipynb
├── 02_dfl_basics_pytorch.ipynb
├── 03_mean_variance_optimization.ipynb
├── 04_partial_index_tracking.ipynb
└── 05_advanced_topics.ipynb
```

### Running the Examples

```bash
# Example 1: Simple DFL Model
python examples/simple_dfl.py

# Example 2: Mean-Variance Optimization
python examples/mean_variance.py

# Example 3: Partial Index Tracking
python examples/partial_index_tracking.py
```

## 📁 Repository Structure

```
dfl-icaif2025/
├── README.md
├── requirements.txt
├── LICENSE
├── assets/
│   ├── logo-website-style.svg
│   ├── logo-square-website-style.svg
│   └── social-preview.svg
├── notebooks/                 # Jupyter notebooks for tutorial
│   ├── 01_introduction_to_dfl.ipynb
│   ├── 02_dfl_basics_pytorch.ipynb
│   ├── 03_mean_variance_optimization.ipynb
│   ├── 04_partial_index_tracking.ipynb
│   └── 05_advanced_topics.ipynb
├── src/                       # Source code
│   ├── __init__.py
│   ├── models/               # DFL models
│   │   ├── __init__.py
│   │   ├── dfl_base.py
│   │   └── neural_nets.py
│   ├── optimization/         # Optimization layers
│   │   ├── __init__.py
│   │   ├── markowitz.py
│   │   └── index_tracking.py
│   └── utils/                # Utility functions
│       ├── __init__.py
│       ├── data_loader.py
│       └── metrics.py
├── examples/                  # Standalone examples
│   ├── simple_dfl.py
│   ├── mean_variance.py
│   └── partial_index_tracking.py
├── data/                      # Data files (if needed)
│   └── README.md
├── slides/                    # Tutorial slides
│   └── dfl_tutorial.pdf
└── tests/                     # Unit tests
    └── test_models.py
```

## 📊 Datasets

The tutorial uses publicly available financial data:

- **S&P 100 stocks** - Historical price and return data
- **Market indices** - Benchmark performance data
- **Financial statements** - Company fundamentals (if needed)

Data will be automatically downloaded using `yfinance` when running the notebooks.

## 🔬 Key Concepts

### Prediction-Focused Learning (PFL)
Traditional two-stage approach:
1. Train ML model to predict parameters (e.g., returns, covariance)
2. Use predictions as input to optimization problem

**Problem:** Optimizing prediction accuracy doesn't necessarily optimize decision quality.

### Decision-Focused Learning (DFL)
End-to-end approach:
1. Integrate prediction and optimization into single differentiable pipeline
2. Train ML model to directly optimize decision quality
3. Gradients flow from decision loss back through optimization to predictions

**Advantage:** Learns predictions that lead to better decisions, not just accurate predictions.

## 📖 References

If you use this code or find the tutorial helpful, please cite:

```bibtex
@inproceedings{lee2025dfl,
  title={Decision-Focused Learning in Financial Optimization},
  author={Lee, Yongjae and Kim, Woo Chang and Lee, Junhyeong and Bae, Hyunglip and Jeon, Haeun},
  booktitle={Proceedings of the 6th ACM International Conference on AI in Finance},
  year={2025}
}
```

### Related Papers
- Wilder, B., Dilkina, B., & Tambe, M. (2019). Melding the data-decisions pipeline: Decision-focused learning for combinatorial optimization. AAAI.
- Elmachtoub, A. N., & Grigas, P. (2022). Smart "predict, then optimize". Management Science.
- Donti, P., Amos, B., & Kolter, J. Z. (2017). Task-based end-to-end model learning in stochastic optimization. NeurIPS.

## 👥 Organizers

<div align="center">

| | | | | |
|:---:|:---:|:---:|:---:|:---:|
| <img src="https://via.placeholder.com/120" width="120" style="border-radius: 10px;"><br/>**Yongjae Lee**<br/>UNIST<br/>[![LinkedIn](https://img.shields.io/badge/-LinkedIn-0077B5?style=flat&logo=linkedin)](https://www.linkedin.com/in/yongjae-lee-548982107) | <img src="https://via.placeholder.com/120" width="120" style="border-radius: 10px;"><br/>**Woo Chang Kim**<br/>KAIST<br/>[![LinkedIn](https://img.shields.io/badge/-LinkedIn-0077B5?style=flat&logo=linkedin)](https://www.linkedin.com/in/woo-chang-kim-a7774810) | <img src="https://via.placeholder.com/120" width="120" style="border-radius: 10px;"><br/>**Junhyeong Lee**<br/>UNIST<br/>[![LinkedIn](https://img.shields.io/badge/-LinkedIn-0077B5?style=flat&logo=linkedin)](https://www.linkedin.com/in/junhyeong-lee-137b56202) | <img src="https://via.placeholder.com/120" width="120" style="border-radius: 10px;"><br/>**Hyunglip Bae**<br/>KAIST<br/>[![LinkedIn](https://img.shields.io/badge/-LinkedIn-0077B5?style=flat&logo=linkedin)](https://www.linkedin.com/in/hyunglip-bae-85981b278) | <img src="https://via.placeholder.com/120" width="120" style="border-radius: 10px;"><br/>**Haeun Jeon**<br/>KAIST<br/>[![LinkedIn](https://img.shields.io/badge/-LinkedIn-0077B5?style=flat&logo=linkedin)](https://www.linkedin.com/in/haeun-jeon-08a4a3292) |

</div>

## 📧 Contact

For questions or issues, please:
- Open an issue on GitHub
- Email: jun.lee@unist.ac.kr

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- ICAIF 2025 organizing committee
- UNIST and KAIST research teams
- Open source community for PyTorch, cvxpy, and cvxpylayers

## 🔗 Resources

- **Tutorial Website:** [https://bridge-po.github.io/](https://bridge-po.github.io/)
- **ICAIF 2025:** [https://icaif25.org/](https://icaif25.org/)
- **cvxpylayers Documentation:** [https://github.com/cvxgrp/cvxpylayers](https://github.com/cvxgrp/cvxpylayers)
- **PyTorch Documentation:** [https://pytorch.org/docs/](https://pytorch.org/docs/)

---

<div align="center">

**⭐ If you find this tutorial helpful, please star this repository!**

<img src="assets/logo-square-website-style.svg" alt="DFL" width="120"/>

© 2025 DFL @ ICAIF'25 • UNIST & KAIST

</div>
