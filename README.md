# Testing Driving Mechanisms of Megathrust Seismicity With Explainable AI

## 🌍 Overview

This repository provides the data and code for the research paper, "Testing Driving Mechanisms of Megathrust Seismicity With Explainable Artificial Intelligence".

The project addresses a fundamental challenge in geophysics: understanding the factors that control the generation of mega-earthquakes (Mw ≥ 8.0) at subduction zones. While many geophysical properties are thought to be linked to large seismic events, traditional statistical methods have found only weak, inconsistent correlations. This suggests the relationships are complex and non-linear, making it an ideal problem for machine learning.

We developed an **Explainable Artificial Intelligence (XAI)** pipeline to not only predict seismic magnitude classes but also to interpret the model's decisions, uncovering the underlying physics driving its performance.

---

## 🔬 An Explainable AI (XAI) Approach

Our methodology combines a deep learning model for classification with a state-of-the-art XAI technique to provide interpretable results.

### 1. Feature Engineering
We compiled a comprehensive dataset of 49 features for 556 subduction zone segments across eight major regions. The features represent the physical state, kinematics, and dynamics of the subduction process and are grouped into three types:

* **Type I (Physical State):** Includes parameters like subduction interface curvature, sediment thickness, bathymetric roughness, and gravity anomalies, which have been previously proposed to influence seismicity.
* **Type II (Dynamics):** These are **novel proxies for 3D slab stresses** derived from buoyancy-driven subduction calculations. We use slab depth and its first and second derivatives along the trench to represent trench-normal ($\sigma_{N}$) and trench-parallel ($\sigma_{P}$) stresses.
* **Type III (Kinematics & Age):** Includes upper plate velocity, trench velocity, and the age of the subducting slab.

### 2. Classification Model
The core of our approach is a **Fully Connected Network (FCN)** trained to solve a classification problem.
* **Task:** The model classifies megathrust segments into two classes based on the largest earthquake magnitude (Mw) recorded:
    * **C0:** $M_{w} < 8.0$
    * **C1:** $M_{w} \ge 8.0$
* **Architecture:** The FCN consists of an input layer, two hidden layers with ReLU activation, and a softmax output layer.

### 3. Explainability with LRP
To understand *why* the model makes certain predictions, we use **Layer-wise Relevance Propagation (LRP)**, a powerful XAI algorithm. After training the FCN, LRP propagates the output prediction backward through the network to quantify the contribution of each input feature to the final decision. This allows us to identify the most relevant parameters driving the classification of large-magnitude seismic events.

---

## 💡 Key Findings & Insights

The XAI analysis provided two crucial sets of results: validation of existing hypotheses and the discovery of novel relationships.

* **Confirmation of Known Mechanisms:** The LRP analysis confirmed the high relevance of previously identified factors, including **subduction interface curvature, sediment thickness, and long-wavelength bathymetric roughness**. This corroborates the findings of earlier studies and validates the robustness of our XAI approach.

* **Novel Discovery - The Role of 3D Slab Dynamics:** Most importantly, our analysis revealed the high relevance of the proxies for **trench-parallel stresses** (slab depth first and second derivatives). The trench-normal stress component (a proxy for simple slab pull) showed a much weaker relationship.

* **Scientific Implication:** This suggests that the occurrence of mega-earthquakes is strongly influenced by **3D subduction dynamics**. Tectonic loading is maximized at **slab steps and edges**, where abrupt changes in slab depth allow deeper, neighboring slabs to exert significant trench-parallel force. This provides a new mechanical framework for understanding why the world's largest earthquakes occur on specific megathrust segments.

---

## 💻 Tech Stack

This project was developed using the following tools and libraries:

| Category | Technology |
| :--- | :--- |
| **Analysis & Modeling** | ![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white) ![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white) ![Scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white) |
| **Data Handling** | ![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white) ![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white) |
| **Geospatial & Plotting**| ![GMT](https://img.shields.io/badge/GMT-00599C?style=for-the-badge&logo=gmt&logoColor=white) ![cmocean](https://img.shields.io/badge/cmocean-46A3A3?style=for-the-badge) |

---

## 💾 Data & Code Availability

The datasets, processed features, code, and trained models used in this study are publicly available on Zenodo.

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.13219207.svg)](https://doi.org/10.5281/zenodo.13219207)

---

## 📜 How to Cite

If you use this work, please cite the original paper:

Graciosa, J. C., Capitanio, F. A., Beall, A., Hargreaves, M., Gollapalli, T., Tang. T., & Zuhair, M. (2025). Testing driving mechanisms of megathrust seismicity with explainable artificial intelligence. *Journal of Geophysical Research: Solid Earth*, 130, e2024JB028774. https://doi.org/10.1029/2024JB028774

----------------------------------
