
## 🧬 Breast Cancer Prediction using Support Vector Machines (SVM)

### 🧩 Overview

This project applies **Support Vector Machine (SVM)** algorithms to classify tumors as **benign or malignant**, based on patient data. Leveraging real-world datasets, it demonstrates the power of SVM in binary classification problems with high dimensionality and medical relevance.

---

### 💼 Business Understanding

Accurate diagnosis of breast cancer is crucial for timely and effective treatment. Misclassification can lead to either delayed care or unnecessary anxiety and procedures. This project helps:

* Automate initial screening in healthcare setups
* Assist medical professionals with ML-backed diagnostic tools
* Improve predictive reliability using optimal hyperparameter tuning

---

### 📊 Data Understanding

* **Dataset**: Breast Cancer Wisconsin Dataset (from `sklearn.datasets`)
* **Size**: 569 samples × 30 features
* **Target Variable**: `target` – 1 (benign), 0 (malignant)
* **Features**:

  * Cell nucleus characteristics: radius, texture, perimeter, area, smoothness, etc.
* **Data Characteristics**:

  * No missing values
  * Highly imbalanced classes handled naturally by SVM margin maximization

---

### 🤖 Modeling and Evaluation

* **Model Used**: Support Vector Classifier (SVC)
* **Hyperparameter Tuning**:

  * Used **GridSearchCV** to find the best combination of `C`, `gamma`, and `kernel`
* **Train-Test Split**:

  * 80% training, 20% testing
* **Evaluation Metrics**:

  * Accuracy
  * Confusion Matrix
  * Precision, Recall, F1-score (via `classification_report`)
* **Results**:

  * High classification performance with tuned hyperparameters

---

### 📌 Conclusion

* SVM successfully classified breast cancer cases with **high precision and recall**
* GridSearchCV significantly improved performance by selecting optimal SVM parameters
* Model proves valuable for **medical diagnostic support**, balancing interpretability and performance

---
