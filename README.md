# PCA Implementation: Financial Inclusion in Africa

## Project Overview
This repository contains a formative assignment for Advanced Linear Algebra. The goal was to implement Principal Component Analysis (PCA) from scratch—without using Scikit-Learn's built-in PCA class—to reduce the dimensionality of a real-world dataset while retaining significant variance.

## The Dataset
**Source:** Financial Inclusion in Africa (Zindi / DPhi)
**Context:** The dataset contains demographic and financial information from individuals across Kenya, Rwanda, Tanzania, and Uganda.
**Preprocessing:**
- **Imputation:** Missing numeric values filled with Mean; categorical with Mode.
- **Encoding:** Categorical variables converted to One-Hot Encoding.
- **Optimization:** Dropped high-cardinality columns (`uniqueid`) to reduce feature space from ~8,000+ to 33 features.

## Methodology
The PCA was implemented using **NumPy** following these mathematical steps:
1.  **Standardization:** $z = \frac{x - \mu}{\sigma}$
2.  **Covariance Matrix:** $\Sigma = \frac{1}{n-1}((X-\bar{x})^T(X-\bar{x}))$
3.  **Eigendecomposition:** Computed Eigenvalues ($\lambda$) and Eigenvectors ($v$).
4.  **Projection:** Transformed the original data onto the new Principal Components.

## Key Results
- **Dimensionality Reduction:** The analysis determined that **26 Principal Components** are required to explain **95%** of the dataset's variance.
- **Visualization:** Successful 2D projection of the complex dataset onto the first two principal components.

## How to Run
1.  Open the `.ipynb` file in Google Colab or Jupyter Notebook.
2.  Ensure the following libraries are installed:
    - `numpy`
    - `pandas`
    - `matplotlib`
    - `seaborn`
3.  Run the cells sequentially. The dataset is loaded automatically from a remote URL.

## Author
Henry Christian Parfait

African Leadership University
