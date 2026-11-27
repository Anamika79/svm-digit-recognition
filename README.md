# Handwritten Digit Recognition Using Linear and Kernel SVMs

Course project (Machine Learning, M.Tech AI). Linear soft-margin SVMs, a hard-margin SVM on handwritten digits (0 vs 1), and RBF-kernel SVMs, implemented with scikit-learn's `SVC`.

## Contents
| Path | Description |
|---|---|
| `notebooks/SVM_Course_Project.ipynb` | Complete Google Colab notebook (Parts 1-3) |
| `report/Project_Report.tex` | IEEE-format technical report (LaTeX source) |
| `report/references.bib`, `report/figures/` | Bibliography and report figures |
| `data/` | Data sets used in the project |

## Tasks
1. **Soft-margin SVM** on two 2-D data sets: decision boundary, test error, effect of `C`.
2. **Digit recognition (0 vs 1, 28x28 images):** hard-margin SVM, misclassified-image analysis, error vs `C`, choosing `C` by 5-fold cross-validation.
3. **RBF kernel SVM** on a non-linearly-separable 2-D set: effect of `gamma` in {1, 10, 100, 1000}.

## Key results
- Data sets 1 and 2: 0 test error; smaller `C` gives a wider margin and more support vectors.
- Digits: hard margin gives 0 training error and 2/2115 test errors (0.095%); `C = 0.03`, chosen by cross-validation, gives 1/2115 (0.047%).
- Data set 3: no linear boundary (linear SVM error 7.1%); RBF with `gamma = 1000` overfits (training error 0).

## Run the notebook
1. Open `notebooks/SVM_Course_Project.ipynb` in [Google Colab](https://colab.research.google.com/) (File > Upload notebook, or open it from GitHub).
2. Run the first cells and upload all files from `data/` when prompted.
3. Run the remaining cells in order.

Requirements: Python 3, NumPy, Matplotlib, scikit-learn (all preinstalled in Colab).

## Build the report
Upload `report/` to Overleaf (or run `pdflatex`, `bibtex`, then `pdflatex` twice). Keep the `figures/` folder next to the `.tex` file.
