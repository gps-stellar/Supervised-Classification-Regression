## 🍷 Wine Quality Classification – Handling Imbalanced Data
### 📌 Project Overview

This project explores the challenge of classifying wine quality using physicochemical properties of wine samples. Unlike balanced datasets, wine quality ratings are highly imbalanced: most wines are rated as average, with very few extreme ratings (very low or very high quality).

The goal of this project is to build, evaluate, and compare multiple machine learning models while applying resampling techniques and advanced model evaluation strategies to handle imbalance effectively.

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

### ⚙️ Process

1. Data Preprocessing

    * Cleaned and prepared the White Wine Quality dataset.

    * Reclassified quality ratings into three categories:

        * Bad (3–4)

        * Median (5–6)

        * Good (7–9)

2. Resampling Strategies

    * RandomUnderSampler (RUS) – reduces the majority class to balance with minorities.

    * SMOTEENN – hybrid approach combining oversampling (SMOTE) with cleaning (Edited Nearest Neighbors).

3. Machine Learning Pipelines
Built pipelines including:

    * Scaling (StandardScaler)

    * Dimensionality Reduction (PCA)

    * Resampling (RUS, SMOTEENN)

    * Classifier (Random Forest, Gradient Boosting, KNN, SVC)

4. Hyperparameter Tuning

    * Applied RandomizedSearchCV for optimization.

    * Evaluated with Balanced Accuracy, F1 (macro), and Precision/Recall (macro).

5. Model Evaluation & Visualization

    * Custom plots for confusion matrices and classification reports.

    * Comparative performance charts across models.

------------------------------------------------------------------------------------------------------------------------

### 📊 Results
| Model	               | Accuracy	| Balanced Accuracy	| F1 (macro)|
|----------------------|-----------|-------------------|-----------|
| Random Forest (RUS)  |	0.497	|0.584	|0.440|
|Gradient Boosting (SMOTEENN) ⭐|	0.660|	0.635|	0.556|
|KNN (RUS)|	0.627	|0.603	|0.538|
|SVC (RUS)|	0.523|	0.601|	0.459|

* Best Model: Gradient Boosting with SMOTEENN

* Achieved highest accuracy, balanced accuracy, and F1 (macro).

* Demonstrated that hybrid resampling + boosting yields strong performance on imbalanced data.

------------------------------------------------------------------------------------------------------------------------

### 🧠 Key Learnings

* Importance of resampling techniques in handling severe class imbalance.

* Use of balanced evaluation metrics (beyond plain accuracy).

* Building modular ML pipelines with scaling, PCA, resampling, and classifiers.

* Applying hyperparameter search strategies (RandomizedSearchCV).

* Effective visualization of model performance through confusion matrices and heatmaps.

------------------------------------------------------------------------------------------------------------------------

### 🚀 Next Steps

* Explore stacking ensembles for even stronger performance.

* Try cost-sensitive learning with class weights.

* Apply calibration techniques to improve probability estimates.

* Extend approach to red wine dataset for comparative study.

------------------------------------------------------------------------------------------------------------------------

### 📂 Repository Structure
bash

├── data/                  # Dataset (if included or linked)  
├── notebooks/             # Jupyter notebooks with experiments  
├── plots/                 # Saved figures and evaluation plots  
├── README.md              # Project overview  
└── requirements.txt       # Dependencies  

------------------------------------------------------------------------------------------------------------------------

### 📑 References

* Wine Quality Data Set – UCI Machine Learning Repository

* Imbalanced-learn documentation: https://imbalanced-learn.org/

* scikit-learn documentation: https://scikit-learn.org/

------------------------------------------------------------------------------------------------------------------------

#### ✨ Author: Giovanni Paz-Silva

------------------------------------------------------------------------------------------------------------------------