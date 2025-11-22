# 🌱 Crop Health Classification Using Machine Learning

This project builds a simple machine learning workflow to classify plant health using remote-sensing indicators.  
It uses **NDVI** (Normalized Difference Vegetation Index) and **Soil Moisture** to predict whether a crop is **healthy** or **unhealthy**, demonstrating the full process from data cleaning to model evaluation and tuning.

---

## 📁 Project Overview

The notebook walks through:

- Loading the dataset  
- Handling missing values and correcting extreme outliers  
- Converting labels into machine-readable formats  
- Training a baseline **Random Forest Classifier**  
- Evaluating the model using:
  - Confusion Matrix  
  - Accuracy, Precision & Recall  
  - ROC Curve & AUC  
- Improving performance with:
  - Cross-validation  
  - Grid Search  
  - Random Search  

This project highlights an end-to-end ML workflow suitable for early applied data science portfolio work.

---

## 🧪 Dataset

The dataset contains **1000 crop samples** with the following features:

| Feature           | Description                                      |
|-------------------|--------------------------------------------------|
| **NDVI**          | Vegetation index representing plant greenness     |
| **Soil_Moisture** | Soil moisture level (%)                           |
| **Health**        | Target variable (healthy / unhealthy)             |

### Data Challenges Addressed

- Missing values (handled with mean imputation)  
- NDVI outliers clipped between −1 and 1  
- Label encoding to binary (`healthy → 1`, `unhealthy → 0`)  

---

## 🛠️ Technologies Used

- Python  
- Pandas & NumPy  
- Scikit-Learn  
- Matplotlib & Seaborn  

---

## 📊 Model Training & Evaluation

A **Random Forest Classifier** was trained using an 80/20 train-test split.

### Confusion Matrix Interpretation

- **True Positives:** correctly predicted healthy crops  
- **True Negatives:** correctly predicted unhealthy crops  
- **False Positives:** unhealthy crops predicted as healthy  
- **False Negatives:** healthy crops predicted as unhealthy  

### Key Metrics

Accuracy: 0.59

Precision: 0.64

Recall: 0.73


### ROC Curve & AUC

The ROC curve visualizes model performance across classification thresholds.

---

## 🔧 Improving the Model

### ✔️ Cross-Validation  
5-fold cross-validation was used to check consistency across data splits.

### ✔️ Grid Search  
Explored parameter combinations (depth, estimators, min samples split).

### ✔️ Random Search  
More efficient search over a wider hyperparameter space.

**Best Parameters Found:**

```json
{
  "max_depth": 5,
  "min_samples_split": 4,
  "n_estimators": 124
}
```
## 📈 Visualizations

Included visual outputs:

Confusion Matrix Heatmap

ROC Curve

Optional exploratory scatter plots

These help interpret how well the model distinguishes between healthy and unhealthy plants.

## 📈 Visualizations

Included visual outputs:

Confusion Matrix Heatmap

ROC Curve

Optional exploratory scatter plots

These help interpret how well the model distinguishes between healthy and unhealthy plants.
