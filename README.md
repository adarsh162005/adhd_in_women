# ADHD in Women

Machine learning pipeline for predicting ADHD outcome and biological sex using high-dimensional neuroimaging, behavioral, and demographic data from the WiDS Datathon 2025 challenge.

---

## Project Overview

This project was developed for the WiDS Datathon 2025 challenge. The objective was to build robust machine learning models capable of predicting:

- ADHD Outcome
- Biological Sex (Female)

using multimodal neuroimaging and behavioral datasets.

The project focuses on:
- high-dimensional data preprocessing
- feature engineering
- class imbalance handling
- interpretable machine learning pipelines

---

## Dataset

This project uses the WiDS Datathon 2025 dataset consisting of:

- Quantitative metadata
- Categorical metadata
- Functional connectome data
- Target labels

Due to dataset size constraints, the raw and processed datasets are not included in this repository.

### Dataset Link
https://www.kaggle.com/competitions/widsdatathon2025/data

After downloading, place the files inside:

```bash
data/raw/
```

---

## Project Workflow

```text
Raw Dataset
     ↓
Data Cleaning & Preprocessing
     ↓
Feature Engineering
     ↓
Handling Class Imbalance
     ↓
Model Training & Evaluation
     ↓
Threshold Tuning
     ↓
Final Predictions
```

---

## Preprocessing Pipeline

The preprocessing pipeline includes:

- Handling missing values
- Duplicate removal
- Data alignment using participant IDs
- One-hot encoding for categorical features
- Label encoding for ordinal variables
- Outlier detection and handling
- Feature correlation analysis
- SHAP-based feature importance analysis
- Standardization using StandardScaler
- Train-validation split preparation

The preprocessing pipeline was designed to efficiently handle high-dimensional neuroimaging data while maintaining computational efficiency.

---

## Models Used

### ADHD Outcome Prediction

Final selected model:
- LightGBM with threshold tuning


---

### Biological Sex Prediction

Final selected model:
- Ensemble model combining Logistic Regression, LightGBM, and Balanced Random Forest

The ensemble model improved robustness and overall classification performance.

---


### Techniques used:
- Feature Scaling using StandardScaler
- Hyperparameter tuning

---


## Evaluation Metrics

The models were evaluated using:

- Recall
- F1 Score
- ROC-AUC Score

Special focus was placed on F1 Score and ROC-AUC Score due to class imbalance in the dataset.

---

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- LightGBM
- SHAP
- Matplotlib
- Seaborn

---

## Repository Structure

```text
wids-2025-adhd-sex-prediction/
│
├── assets/
│   └── dataset_distribution.png
│
├── data/
│   ├── raw/
│   │   └── .gitkeep
│   │
│   ├── processed/
│   │   └── .gitkeep
│   │
│   └── data_dictionary.xlsx
│
├── notebooks/
│   └── adhd_sex_prediction.ipynb
│
├── .gitignore
├── LICENSE
├── requirements.txt
└── README.md
```

---

## Results

The project achieved strong classification performance on both prediction tasks using ensemble learning and optimized preprocessing techniques.

Key highlights:
- Effective handling of high-dimensional connectome data
- Improved performance using threshold tuning
- Robust classification using ensemble models
- Efficient preprocessing pipeline for multimodal datasets

---

## Future Improvements

Potential future enhancements include:

- Deep learning models for connectome analysis
- Advanced feature selection techniques
- Deployment using Flask/FastAPI
- Automated ML pipelines
- Explainable AI dashboards

---

## Author

Adarsh V Kapse

---

## License

This project is licensed under the MIT License.
