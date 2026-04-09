# classifier-comparison
Classic Machine Learning Classifiers Experimental Comparison

## Overview
This project implements and compares several classical classification algorithms on synthetic 2D datasets, including:
- k-Nearest Neighbor (k-NN)
- Naive Bayes
- Linear Discriminant Analysis (LDA)
- Support Vector Machine (SVM)

We analyze decision boundaries, classification accuracy, and how data covariance structure and distribution affect model performance.

## Experimental Results
| Model | Accuracy |
|-------|----------|
| Nearest Neighbor | 72.00% |
| Naive Bayes (shared covariance) | 78.27% |
| Naive Bayes (class-specific covariance) | 75.80% |
| LDA | 72.22% ~ 78.48% |
| SVM | 0.525 |

## Key Findings
1. **Nearest Neighbor**  
   Simple non-linear classifier, sensitive to outliers and high-dimensional data.

2. **Naive Bayes**  
   Highly sensitive to class covariance structure:
   - Shared covariance → linear decision boundary
   - Different covariance → non-linear decision boundary

3. **LDA**  
   Assumes Gaussian distribution and shared class covariance; sensitive to outliers.

4. **SVM**  
   Maximizes classification margin; robust to outliers; suitable for complex distributions.

## Similarities & Differences Between LDA and SVM
- Both are linear classifiers that separate classes with a hyperplane.
- LDA: maximizes between-class variance / minimizes within-class variance.
- SVM: maximizes the margin between support vectors.
- LDA relies on distribution assumptions; SVM is distribution-free.
