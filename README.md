# Classical Computer Vision: Shape and Texture Classification

This repository demonstrates classical computer vision pipelines for image classification using **hand-crafted feature descriptors** and **distance-based learning**.  
The focus is on interpretable, efficient methods that remain relevant when data is limited, explainability matters, or computational constraints apply.

Two complementary problems are explored:
- **Shape classification** using boundary curvature
- **Texture classification** using statistical and local pattern descriptors

---

## Why This Pipeline Is Useful

Classical vision techniques provide strong, lightweight baselines and clear insight into how visual structure is encoded.  
This project highlights how careful feature design can achieve high performance even with simple classifiers such as **K-Nearest Neighbours (KNN)**.

---

## Leaf Shape Classification (HoCS)

This pipeline classifies binary leaf silhouettes using the **Histogram of Curvature Scale (HoCS)** descriptor.

- Boundary curvature is computed using a normalized area integral invariant
- Curvature is evaluated across multiple spatial scales
- Histograms are concatenated into a compact shape descriptor
- Shapes are classified using KNN in feature space

HoCS captures both fine and global shape structure while remaining robust to small boundary perturbations.

---

## Texture Classification (GLCM vs LBP)

This pipeline compares two classical texture descriptors under arbitrary image rotation:

- **GLCM**: global co-occurrence statistics, sensitive to rotation
- **Rotation-invariant LBP + VAR**: local micro-patterns with strong rotational robustness

The comparison illustrates how feature design directly impacts invariance and classification performance.

---

## Evaluation

Both pipelines are evaluated using:
- Classification accuracy
- Confusion matrices
- Analysis of misclassified samples

---

## Data

Datasets are not included due to licensing and academic restrictions.  
See `data/README.md` for expected dataset structure.
