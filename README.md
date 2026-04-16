# Classification of Astronomical Objects using Artificial Neural Networks

## Overview

This project focuses on the supervised classification of astronomical objects into three categories: **Stars, Galaxies, and Quasars** using Artificial Neural Networks (ANNs). The study explores multiple ANN variants, including manually designed models, metaheuristic-optimized architectures, and automated hyperparameter tuning methods.

The objective is to improve classification accuracy, enhance generalization, and provide interpretability using Explainable AI techniques.

---

## Dataset

- Source: Sloan Digital Sky Survey (SDSS DR17)
- Size: Approximately 100,000 samples
- Features: 13 engineered photometric and spectral features
- Classes:
  - Star
  - Galaxy
  - Quasar

### Data Processing

- Handling missing values
- Feature engineering:
  - Color indices (e.g., u-g, g-r)
  - Flux ratios
- Label encoding
- Feature scaling using RobustScaler
- Stratified split:
  - Training: 60%
  - Validation: 20%
  - Test: 20%

---

## Methodology

### ANN Variants

1. **Baseline ANN**
   - Simple feed-forward neural network
   - No explicit regularization

2. **Regularized ANN**
   - Batch Normalization
   - Dropout
   - L2 Regularization
   - Designed for improved generalization

3. **Genetic Algorithm (GA) Optimized ANN**
   - Evolves architecture:
     - Number of layers
     - Neurons per layer
     - Dropout
     - L2 regularization

4. **Particle Swarm Optimization (PSO) ANN**
   - Joint optimization of:
     - Architecture
     - Hyperparameters

5. **Grey Wolf Optimization (GWO) ANN**
   - Metaheuristic optimization based on wolf hierarchy
   - Searches optimal hyperparameters and architecture

6. **Keras Tuner ANN**
   - Hyperband-based automated hyperparameter tuning
   - Optimizes:
     - Neurons
     - Dropout
     - L2 regularization
     - Learning rate

---

## Model Training

- Optimizer: Adam
- Loss Function: Categorical Cross-Entropy
- Callbacks:
  - EarlyStopping
  - ModelCheckpoint
  - ReduceLROnPlateau

---

## Evaluation Metrics

- Accuracy
- Precision
- Recall
- F1-score
- Log Loss
- Confusion Matrix
- ROC Curves
- Overfitting Gap Analysis

---

## Results

- Best Test Accuracy: **0.9768** (Keras Tuner ANN)
- Regularized ANN demonstrated the best generalization performance with minimal overfitting.
- Metaheuristic models produced compact and efficient architectures.
- Random Forest achieved comparable accuracy but with higher complexity and overfitting.

---

## Explainable AI (XAI)

To interpret model predictions:

- **SHAP (SHapley Additive Explanations)**
  - Global and local feature importance

- **LIME (Local Interpretable Model-Agnostic Explanations)**
  - Instance-level explanations

### Key Insight

- Redshift and photometric color indices were identified as the most influential features.

---

---

## Technologies Used

- Python
- TensorFlow / Keras
- Keras Tuner
- Scikit-learn
- NumPy, Pandas
- Matplotlib, Seaborn
- SHAP
- LIME

---

## Key Contributions

- Comparative analysis of six ANN variants
- Integration of metaheuristic optimization (GA, PSO, GWO)
- Application of automated hyperparameter tuning (Keras Tuner)
- Incorporation of Explainable AI for interpretability
- End-to-end pipeline from preprocessing to evaluation

---

## Future Work

- Extend to transformer-based architectures
- Explore Graph Neural Networks for relational data
- Apply to newer SDSS data releases (DR18/DR19)
- Incorporate uncertainty estimation (Bayesian Neural Networks, Monte Carlo Dropout)

---

## References

1. Soriano, F. (2022). Stellar Classification Dataset - SDSS17. Kaggle  
2. Ball, N. M., & Brunner, R. J. (2006). Automated Classification of SDSS Sources  
3. Breiman, L. (2001). Random Forests  
4. Goodfellow, I., Bengio, Y., & Courville, A. (2016). Deep Learning  
5. Pedregosa, F., et al. (2011). Scikit-learn  

---

## Author

Pratham Mishra  
Manipal University Jaipur  
Computer Science (AI/ML)
