
## 🧬 Breast Cancer Prediction using Support Vector Machines (SVM)

### 🧩 Overview

This project addresses the problem of **predicting breast cancer** as either benign or malignant based on characteristics of cell nuclei. We utilized the well-known breast cancer dataset available through scikit-learn, which contains various features derived from digitized images of breast masses. Our modeling status involves training and evaluating a **Support Vector Machine (SVM) classifier** to differentiate between the two cancer types.

---

### 💼 Business Understanding

The primary stakeholders in this project are medical professionals, such as oncologists and radiologists, who require reliable tools to assist in diagnosing breast cancer. The core business problem addressed is the need for a more accurate and automated method to distinguish between benign and malignant cases based on patient data. By developing a predictive model, we aim to support medical experts in making timely and informed decisions, potentially leading to earlier detection and improved patient outcomes. Research indicates that accurate initial diagnosis is crucial in determining appropriate treatment plans and can significantly impact patient survival rates.Accurate diagnosis of breast cancer is crucial for timely and effective treatment. Misclassification can lead to either delayed care or unnecessary anxiety and procedures. This project helps:

* Automate initial screening in healthcare setups
* Assist medical professionals with ML-backed diagnostic tools
* Improve predictive reliability using optimal hyperparameter tuning

---

### 📊 Data Understanding

This project utilizes the breast cancer dataset provided by scikit-learn. This dataset is a classic benchmark in machine learning and is derived from the University of Wisconsin Hospitals, Madison. The specific timeframe of data collection is not explicitly stated in the dataset's documentation but represents historical patient data.
The dataset consists of 30 numerical features computed from digitized images of fine needle aspirate (FNA) of a breast mass, describing characteristics of cell nuclei. The target variable is a binary classification indicating whether the mass is benign (0) or malignant (1).

**SUMMARY OF DATASET: -**

* **Dataset**: Breast Cancer Wisconsin Dataset (from `sklearn.datasets`)
* **Size**: 569 samples × 30 features
* **Target Variable**: `target` – 1 (benign), 0 (malignant)
* **Features**:

  * Cell nucleus characteristics: radius, texture, perimeter, area, smoothness, etc.
 
    ![image](https://github.com/user-attachments/assets/81222ea4-63b1-4bdf-81a7-09f0cc18acfe)

* **Data Characteristics**:

  * No missing values
  * Highly imbalanced classes handled naturally by SVM margin maximization
 
* **Data Limitations:**
Key limitations include the dataset being static (not a continuous stream of data), potential bias based on the original patient population, challenges in interpreting features without medical expertise, and the lack of additional clinical context beyond image analysis features


---

![image](https://github.com/user-attachments/assets/57ae7143-9cb0-4787-90a3-6767c1f5620a)


### 🤖 Modeling and Evaluation

* **Model Used**: Support Vector Classifier (SVC) with a Radial Basis Function (RBF) kernel. The hyperparameters used were gamma = 0.5 and C = 1.0.
* **Hyperparameter Tuning**:

  * **Feature scaling using StandardScaler** was applied to the training and testing data before training the final model.
    
* **Train-Test Split**:

  * 80% training, 20% testing
* **Evaluation Metrics**:

  * **Accuracy:** Approximately 0.66.
  * **Confusion Matrix:**
       - True Negatives (TN): 9
       - False Positives (FP): 39
       - False Negatives (FN): 0
       - True Positives (TP): 66
* **Classification Report:** Providing Precision, Recall, and F1-score for each class (Benign and Malignant).
Evaluation Results Interpretation: The model achieved a perfect recall for the malignant class (identifying all malignant cases) but had a high number of false positives (misclassifying benign cases as malignant) and low recall for the benign class. This indicates a strong bias towards predicting the malignant class, prioritizing the avoidance of false negatives over minimizing false positives.
 
* **Results**:

  * Good classification performance with scaled values.

---

### 📌 Conclusion

Based on the **Support Vector Machine (SVM)** model's performance, while it **excels at identifying all malignant cases (which is critical in a medical context), the high rate of false positives is a significant drawback.** A large number of false positives can lead to unnecessary stress, anxiety, and costly follow-up procedures for patients who are ultimately found to be benign. To better address the business problem in a real-world medical setting, a model with a more balanced performance is desirable, aiming to reduce false positives while maintaining a high recall for the malignant class.
In the future we can collect more data, can perform hyperparameter tunning, address class imbalance, perform feature engineering so to improve the performance of the model.

---
