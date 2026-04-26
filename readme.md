# NovaGen Health Classification

A supervised machine learning project developed for NovaGen Research Labs to classify individuals as **healthy** or **unhealthy** based on clinical and lifestyle health indicators.

## Dataset

- 9,549 patient records with 22 features
- Features include physiological measurements (BMI, Blood Pressure, Cholesterol, Glucose Level), lifestyle factors (Smoking, Alcohol, Exercise Hours, Sleep Hours), and encoded categorical variables (Diet Type, Blood Group)
- Target variable: 0 = Healthy, 1 = Unhealthy

## Project Structure

```
NovaGen/
├── novagen_dataset.csv              # Dataset
├── novaGen.ipynb # Main ML pipeline
├── eda_overview.png                 # Exploratory data analysis charts
├── model_comparison.png             # Model performance comparison
└── best_model_analysis.png          # Feature importance and confusion matrix
```

## Pipeline Overview

| Step | Description                             |
| ---- | --------------------------------------- |
| 1    | Load and inspect dataset                |
| 2    | Exploratory Data Analysis (EDA)         |
| 3    | Preprocessing and train/test split      |
| 4    | Train 6 classification models           |
| 5    | Compare models across key metrics       |
| 6    | Hyperparameter tuning on best model     |
| 7    | Feature importance and confusion matrix |
| 8    | Final performance summary               |

## Models Trained

- Logistic Regression
- Decision Tree
- Random Forest
- Gradient Boosting
- K-Nearest Neighbors (KNN)
- Support Vector Machine (SVM)

## Results

| Model               | Accuracy | F1 Score | AUC-ROC |
| ------------------- | -------- | -------- | ------- |
| Logistic Regression | 0.8136   | 0.8224   | 0.8879  |
| Decision Tree       | 0.8597   | 0.8665   | 0.9229  |
| Random Forest       | 0.9366   | 0.9402   | 0.9845  |
| Gradient Boosting   | 0.9199   | 0.9248   | 0.9721  |
| KNN                 | 0.8901   | 0.8947   | 0.9485  |
| SVM                 | 0.9335   | 0.9371   | 0.9776  |

**Best Model: Random Forest** (after hyperparameter tuning — max_depth=20, n_estimators=200)

- Accuracy: 0.94
- F1 Score: 0.94
- AUC-ROC: 0.9845

## Requirements

```
numpy
pandas
matplotlib
seaborn
scikit-learn
```

Install with:

```bash
pip install numpy pandas matplotlib seaborn scikit-learn
```

## Usage

```bash
python novaGen.ipynb
```

Ensure `novagen_dataset.csv` is in the same directory before running.
