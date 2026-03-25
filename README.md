# Archaeometric-Elemental-Analysis-Pipeline
Archaeometric Data Analysis Pipeline in R: A comprehensive script for elemental analysis featuring PCA (with Mahalanobis outlier detection), Hierarchical Clustering, correlation heatmaps, and automated visualization for archaeological provenance or compositional studies.

# Archaeometric Elemental Analysis Pipeline

This R script provides a robust workflow for analyzing elemental composition data typically used in archaeology and geology. It performs data cleaning, multivariate statistics, and high-quality visualizations to identify patterns and group relationships.

## 🚀 Features

* **PCA Analysis:** Performs Principal Component Analysis using `FactoMineR` and `factoextra`.
* **Outlier Detection:** Implements **Mahalanobis Distance** ($\chi^2$ distribution) to automatically flag multivariate outliers.
* **Hierarchical Clustering:** Generates dendrograms based on Ward's method to visualize group similarities.
* **Pairwise Comparisons:** Creates a matrix of scatter plots, densities, and correlations using `GGally`.
* **Correlation Heatmaps:** Visualizes relationships between chemical elements (6 of them would be fine).
* **Reference Benchmarking:** Calculates Euclidean distances of all groups relative to a specific reference group (e.g., `LocNo 2`).
* **Automated Export:** Saves results directly to CSV and PDF (to your Desktop or Project folder).

## 🛠️ Required Packages

The script automatically checks and installs the following libraries:
`readxl`, `dplyr`, `FactoMineR`, `factoextra`, `ggplot2`, `RColorBrewer`, `ggrepel`, `reshape2`, `dendextend`, `GGally`, `viridis`, `gridExtra`.

## 📂 Data Structure

The script expects an Excel file (`Input.xlsx`) with the following:
* **LocNo:** A column representing location or group IDs (e.g., 1, 2, 3...).
* **Elements:** Numerical columns for chemical elements (Six of them would be fine).



## 📖 How to Use

1.  Place your data in `C:/Users/pc/Input.xlsx` (or modify the `file_path` variable in the script).
2.  Define your `target_groups` (LocNo) to focus on specific archaeological sites or contexts.
3.  Run the script in **RStudio**.
4.  Check your **Desktop** for:
    * `PCA_result_selectedLocNo_individuals.csv` (Coordinates and Outlier status).
    * `Pairwise_PCA_selectedLocNo.pdf` (High-resolution publication-ready plots).
    * `correlation_matrix_groupMeans_selectedElements.csv`.

## 📊 Visualizations Included

* **PCA Biplot:** Individual points colored by group, with outliers highlighted in red.
* **Dendrogram:** Hierarchical clustering of group means.
* **Heatmap:** Correlation tile plot showing elemental relationships.
* **Pairwise Matrix:** Detailed look at element distributions and linear correlations.

## ⚖️ License
This project is open-source. Feel free to use and adapt it for your archaeological research!
