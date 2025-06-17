# Ovarian Cancer Subtype Classification

This project focuses on developing an automated system to classify ovarian cancer subtypes using histopathological images and machine learning techniques. Ovarian cancer is one of the most dangerous gynecological cancers, and accurate subtype classification is essential for diagnosis and treatment.

## 📌 Problem Statement

Manual examination of histopathological images is often subjective, time-consuming, and error-prone. This project addresses the need for a faster, more reliable diagnostic system by leveraging image processing and machine learning algorithms.

## 🎯 Objectives

### Primary Objective
Develop a computerized system that automatically identifies and classifies ovarian cancer subtypes using texture-based image features and traditional machine learning models.

### Specific Objectives
- Collect and preprocess a labeled dataset of ovarian cancer histopathological images.
- Apply image segmentation and texture analysis techniques.
- Extract mathematical features (e.g., GLCM, fractal dimension).
- Train and evaluate classification models: SVM, Decision Tree, Random Forest, and XGBoost.
- Compare model performance using accuracy, precision, recall, and F1-score.

## 🧠 Theoretical Background

- **Texture Analysis:** Captures subtle visual patterns in tissues missed by shape or color alone.
- **Haralick Features:** Derived from the Gray Level Co-occurrence Matrix (GLCM), they quantify contrast, correlation, energy, and homogeneity in images.
- **Fractal Dimension & Entropy:** Measure structural complexity and randomness of cancerous tissue patterns.
- **Machine Learning:** Trained models on handcrafted features instead of raw pixel data for better interpretability and efficiency.

## 🧪 Technologies Used

| Category         | Libraries/Tools                |
|------------------|--------------------------------|
| Image Processing | OpenCV, Scikit-Image           |
| Feature Handling | NumPy, Pandas                  |
| Visualization    | Matplotlib, Seaborn            |
| ML Algorithms    | Scikit-Learn, XGBoost          |

## 🧬 Dataset

- **Source:** Mendeley Data & Kaggle
- **Samples:** 498 histopathological images labeled into:
  - Clear Cell (100)
  - Serous (100)
  - Endometrioid (98)
  - Mucinous (100)
  - Non-Cancerous (100)

## 🧰 Data Preprocessing

- Noise reduction and grayscale conversion
- Data augmentation to reduce overfitting and class imbalance:
  - Rotation (±10°)
  - Width/height shifts (5%)
  - Shearing (2%)
  - Zoom (90%–120%)
  - Flipping, brightness adjustment

## 🔍 Feature Engineering

- **GLCM Features**: Contrast, correlation, energy, homogeneity
- **Fractal Features**: Complexity of tissue patterns
- **Entropy**: Image randomness
- These features were combined to form the input for ML models.

## 📈 Model Training & Results

Four ML models were trained and compared:
- Support Vector Machine (SVM)
- Decision Tree
- Random Forest
- **XGBoost** (Best performing)

### ✅ Best Model: Fine-Tuned XGBoost

| Metric      | Value    |
|-------------|----------|
| Accuracy    | 74%      |
| Best F1-Score | 0.85 (Endometrioid) |
| Most Misclassified | Mucinous, Non-Cancerous |

> XGBoost showed the best balance between accuracy and robustness, successfully capturing textural and structural differences among subtypes.

## ⚠️ Challenges

- Data imbalance, particularly in rare subtypes
- Variation in image quality
- Feature redundancy

## 🔭 Future Work

- Regional (patch-wise) feature extraction for higher granularity
- Explore hybrid deep learning and handcrafted feature models
- Apply explainable AI for better model interpretability



