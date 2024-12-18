## Data-Driven Earthquake Hazard Mapping Using PyTorch Neural Networks and Sklearn Tools

This project leverages Machine Learning and Explainable AI (XAI) to identify mechanisms driving megathrust fault seismicity (large earthquakes, Mw > 8.0) across global subduction zones. The goal is to classify fault segments based on earthquake magnitude using ML and to determine which geophysical features are most influential.

**Key Steps:**

***Data Preprocessing and Feature Engineering:***

- Collected and processed heterogeneous datasets, including physical features (e.g., strain rates, curvature), dynamic slab properties, and kinematic trench motions.

- Applied grid-based spatial sampling to ensure consistent feature extraction across regions.

- Engineered geophysical metrics such as cumulative seismic moment, energy, and event classifications to enrich model inputs.

*Model Development:*

- Designed and trained a modular **Fully Connected Neural Network (FCN)** in PyTorch, supporting both classification and regression tasks.

- Employed robust techniques such as dropout, batch normalization, and multi-task learning to enhance model generalization.

- Conducted hyperparameter tuning using random search to optimize network performance.

***Evaluation and Validation:***

- Implemented cross-validation to assess model performance, using metrics such as F1-score, accuracy, and confusion matrices.

- Validated the model on unseen regions to ensure robustness and scalability.

- Explainability with Layerwise Relevance Propagation (LRP):

- Utilized LRP to identify key geophysical features influencing predictions, enhancing the model’s interpretability.

- Visualized relevance heatmaps to highlight critical regions and features, aiding scientific understanding and decision-making.

***Visualization and Deployment:***

- Generated geospatial classification maps and relevance heatmaps using Cartopy and Matplotlib to communicate results effectively.

- Created modular pipelines for model deployment and inference on new datasets.

**Key Results:**

- Achieved accurate classification of earthquake-prone regions, with F1-scores ranging between 0.568 and 0.864.

- Identified critical features such as slab depth curvature, sediment thickness, and trench-parallel stresses as significant drivers of seismic activity.

- Reduced manual data processing time by automating the entire pipeline, enabling scalable and reproducible ML workflows.


This work has recently been accepted into a Tier 1 peer-reviewed journal. It was also selected for a presentation at the European Geosciences Union's General Assembly 2022 in Vienna, Austria: https://ui.adsabs.harvard.edu/abs/2022EGUGA..2411060G/abstract

--------------------------


**helper_pkg**: serves as a foundation for Machine Learning (ML) workflows by enabling efficient data preparation, feature engineering, and spatial sampling.

**ml4szeq**: folder provides a complete end-to-end machine learning pipeline, including data preprocessing, model development, training, evaluation, and prediction for earthquake analysis using PyTorch.

**model**: The folder contains saved PyTorch model checkpoints, enabling model reuse, scenario-based performance evaluation, and inference without retraining.

**ntbk**: The folder contains Jupyter notebooks that implement key project steps, including grid-based spatial sampling, model evaluation, and visualization of Layerwise Relevance Propagation (LRP) heatmaps for interpretability.
