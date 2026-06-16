# Letter Recognition Classification

Classifying 26 capital English letters using pixel-derived features from the UCI Letter Recognition dataset.

## Models
- Random Forest — 96.8% accuracy
- KNN — 94.95% accuracy

## Dataset
[UCI Letter Recognition](https://archive.ics.uci.edu/dataset/59/letter+recognition) — 20,000 samples, 16 features

## How to run
1. pip install pandas matplotlib seaborn scikit-learn
2. Open the notebook in Jupyter or VS Code
3. Run all cells

## Key Findings

**Feature correlations:**
- x-box and width are strongly correlated (0.85) — wider letters occupy more horizontal space
- y-box and high are strongly correlated (0.82) — taller letters have larger bounding boxes
- width, high, and onpix are all positively linked — larger letters activate more pixels
- x-bar and y-bar are negatively correlated (-0.36) — as horizontal pixel center increases, vertical center tends to decrease

**Model results:**
- Random Forest: 96.8% accuracy (best params: 150 trees, unlimited depth, sqrt features)
- KNN: 94.95% accuracy (best k=3)
- Most misclassifications occur between visually similar letters (B/D, M/N)
- Random Forest's ensemble approach handles overlapping letter shapes better than KNN

**Data notes:**
- 20,000 samples, 26 classes, perfectly balanced (~770–815 per letter)
- 1,332 duplicate rows retained — likely genuine repeated pixel patterns, not errors
- No missing values