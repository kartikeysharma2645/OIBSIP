# 🌸 Iris Flower Classification

A machine learning classification project that predicts the species of an Iris flower using its sepal and petal measurements.

This project was developed as **Task 1 of my Data Science Internship at Oasis Infobyte (OIBSIP)** and covers the complete machine learning workflow — from exploratory data analysis and preprocessing to model evaluation, hyperparameter tuning, and prediction on unseen data.

---

## 📌 Project Objective

The objective of this project is to build a machine learning model capable of classifying an Iris flower into one of three species:

- **Iris Setosa**
- **Iris Versicolor**
- **Iris Virginica**

The prediction is based on four numerical measurements:

- Sepal Length
- Sepal Width
- Petal Length
- Petal Width

---

## 📊 Dataset

The project uses the classic **Iris dataset**, containing **150 flower samples** distributed across three species.

| Feature | Description |
|---|---|
| Sepal Length | Length of the sepal in centimeters |
| Sepal Width | Width of the sepal in centimeters |
| Petal Length | Length of the petal in centimeters |
| Petal Width | Width of the petal in centimeters |
| Species | Target class of the Iris flower |

The dataset contains **50 samples for each species**, making it balanced across the three target classes.

---

## 🔍 Exploratory Data Analysis

Exploratory Data Analysis (EDA) was performed to understand the structure, distributions, and relationships within the dataset.

The analysis included:

- Dataset inspection and summary statistics
- Missing-value and duplicate checks
- Species distribution analysis
- Feature distribution visualization
- Scatter plots
- Pairwise feature analysis

### Key EDA Findings

- **Setosa** is clearly distinguishable from the other two species, particularly through petal measurements.
- **Versicolor and Virginica** show some overlap.
- **Petal Length and Petal Width** provide the strongest visual separation between the three species.
- The dataset is balanced across all three classes.

---

## ⚙️ Machine Learning Workflow

The project follows this workflow:

```text
Data Loading
     ↓
Data Understanding & Cleaning
     ↓
Exploratory Data Analysis
     ↓
Feature / Target Separation
     ↓
Train-Test Split (80% / 20%)
     ↓
Feature Scaling
     ↓
Model Training
     ↓
Model Evaluation
     ↓
Hyperparameter Tuning
     ↓
Model Comparison
     ↓
Final Model Selection
     ↓
Prediction on New Data
```

---

## 🧠 Models Implemented

Four classification algorithms were trained and evaluated:

### 1. K-Nearest Neighbors (KNN)

KNN classifies new samples based on the classes of their nearest neighbors.

Because KNN is distance-based, the input features were standardized using `StandardScaler`.

The model was further optimized using:

- Scikit-learn `Pipeline`
- `StandardScaler`
- `GridSearchCV`
- 5-Fold Cross-Validation

### 2. Decision Tree

A Decision Tree classifier was trained to classify flowers using feature-based decision rules.

The trained tree was visualized to understand its classification decisions, and feature importance was analyzed.

### 3. Random Forest

Random Forest combines predictions from multiple Decision Trees to produce a more robust ensemble classifier.

Feature importance analysis showed that petal measurements contributed most strongly to classification.

### 4. Logistic Regression

Logistic Regression was trained using standardized features.

In addition to class predictions, predicted class probabilities were analyzed to understand the model's confidence across the three species.

---

## 📈 Model Performance

All four models achieved perfect accuracy on the held-out test set for the selected train-test split.

| Model | Test Accuracy |
|---|---:|
| KNN (K = 5) | 100% |
| **Tuned KNN (K = 3)** | **100%** |
| Decision Tree | 100% |
| Random Forest | 100% |
| Logistic Regression | 100% |

> **Note:** The 100% test accuracy reflects performance on this specific held-out test split and should not be interpreted as guaranteed performance on every unseen dataset.

---

## 🔧 KNN Hyperparameter Tuning

KNN was optimized using `GridSearchCV` with **5-fold cross-validation**.

Values tested for `n_neighbors`:

```python
[1, 3, 5, 7, 9, 11]
```

### Tuning Results

| Metric | Result |
|---|---:|
| Best K | **3** |
| Best Cross-Validation Accuracy | **95.00%** |
| Tuned Test Accuracy | **100.00%** |

A Scikit-learn `Pipeline` was used to combine feature scaling and KNN so that `StandardScaler` was fitted independently within each cross-validation training fold, preventing data leakage from the validation folds.

---

## 🌳 Feature Importance

Feature importance analysis from the tree-based models reinforced the patterns observed during EDA.

### Decision Tree

| Feature | Importance |
|---|---:|
| Sepal Length | 0.00% |
| Sepal Width | 1.67% |
| Petal Length | **90.61%** |
| Petal Width | 7.72% |

### Random Forest

| Feature | Importance |
|---|---:|
| Sepal Length | 10.81% |
| Sepal Width | 3.04% |
| Petal Length | **44.00%** |
| Petal Width | **42.15%** |

Both analyses indicate that **petal measurements are highly informative for Iris species classification**.

---

## 🏆 Final Model

The **Tuned KNN Pipeline with K = 3** was selected as the final model.

Although all evaluated models achieved the same test accuracy, KNN was selected after systematic hyperparameter optimization using GridSearchCV and 5-fold cross-validation.

The final pipeline handles:

```text
New Flower Measurements
          ↓
    StandardScaler
          ↓
   KNN Classifier (K=3)
          ↓
   Predicted Species
```

---

## 🌼 Example Prediction

A new flower with the following measurements was provided to the final model:

```text
Sepal Length : 5.1 cm
Sepal Width  : 3.5 cm
Petal Length : 1.4 cm
Petal Width  : 0.2 cm
```

Prediction:

```text
Predicted Species: setosa
```

The example demonstrates how the trained pipeline can classify new flower measurements that were not directly used as training samples.

---

## 🛠️ Technologies Used

- **Python**
- **Pandas** — data manipulation and analysis
- **NumPy** — numerical operations
- **Matplotlib** — data visualization
- **Seaborn** — statistical visualization
- **Scikit-learn** — preprocessing, machine learning, model evaluation and tuning
- **Jupyter Notebook** — experimentation and documentation

---

## 📁 Project Structure

```text
DataScience-Task1-IrisFlowerClassification/
│
├── IrisFlowerClassification.ipynb
└── README.md
```

The Jupyter Notebook contains the complete implementation, including EDA, preprocessing, model training, evaluation, tuning, comparison, and final prediction.

---

## 💡 Key Learnings

This project provided practical experience with:

- Performing exploratory data analysis on a real classification dataset
- Understanding relationships between numerical features and target classes
- Splitting data correctly into training and testing sets
- Standardizing numerical features using `StandardScaler`
- Preventing data leakage during preprocessing and cross-validation
- Training multiple classification algorithms
- Evaluating models using accuracy, confusion matrices, precision, recall, and F1-score
- Performing hyperparameter tuning using `GridSearchCV`
- Building leakage-safe workflows using Scikit-learn `Pipeline`
- Interpreting Decision Tree and Random Forest feature importance
- Comparing multiple machine learning models
- Making predictions on unseen samples

---

## 📌 Internship

This project was completed as part of the **Oasis Infobyte Data Science Internship (OIBSIP)**.

**Task:** 1 — Iris Flower Classification

---

## 👨‍💻 Author

**Kartikey Sharma**

B.Tech — Artificial Intelligence & Machine Learning  
World College of Technology and Management, Gurgaon

---

⭐ If you found this project useful, consider giving the repository a star.