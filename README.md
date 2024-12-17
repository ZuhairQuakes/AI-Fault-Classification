## Data-Driven Earthquake Hazard Mapping Using PyTorch Neural Networks and Sklearn Tools

This project leverages Machine Learning and Explainable AI (XAI) to identify mechanisms driving megathrust fault seismicity (large earthquakes, Mw > 8.0) across global subduction zones. The goal is to classify fault segments based on earthquake magnitude using ML and to determine which geophysical features are most influential.

I integrated diverse datasets (geophysical, kinematic, and dynamic features) for training a neural network to classify earthquake-prone regions. I applied Layerwise Relevance Propagation (LRP) to uncover the most significant features driving predictions, enhancing model interpretability.

Through this project, I developed skills in handling large-scale geospatial data, designing robust ML pipelines, and deriving actionable insights.

This work has recently been accepted into a Tier 1 peer-reviewed journal. It was also selected for a presentation at the European Geosciences Union's General Assembly 2022 in Vienna, Austria: https://ui.adsabs.harvard.edu/abs/2022EGUGA..2411060G/abstract

--------------------------


**helper_pkg**: serves as a foundation for Machine Learning (ML) workflows by enabling efficient data preparation, feature engineering, and spatial sampling.

**ml4szeq**: folder provides a complete end-to-end machine learning pipeline, including data preprocessing, model development, training, evaluation, and prediction for earthquake analysis using PyTorch.

**model**: The folder contains saved PyTorch model checkpoints, enabling model reuse, scenario-based performance evaluation, and inference without retraining.

**ntbk**: The folder contains Jupyter notebooks that implement key project steps, including grid-based spatial sampling, model evaluation, and visualization of Layerwise Relevance Propagation (LRP) heatmaps for interpretability.
