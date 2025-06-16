# 🍄 Support Vector Machine (SVM) Classification: Mushroom Edibility Prediction

## 🎯 Objective

To implement and evaluate a **Support Vector Machine (SVM)** classifier for predicting whether mushrooms are **edible or poisonous** using the Mushroom Dataset. This project includes EDA, preprocessing, visualization, model training, hyperparameter tuning, kernel comparison, and performance evaluation.

---

## 📁 Dataset Description

### Dataset: `mushroom.csv`

This dataset contains features describing mushrooms and their edibility status. Most columns are **categorical**, with two notable **numerical** features: `stalk_height` and `cap_diameter`.

| Column Name              | Description                                            |
|--------------------------|--------------------------------------------------------|
| `class`                  | Target: edible or poisonous                            |
| `cap_shape`              | Bell, conical, convex, flat, knobbed, sunken           |
| `cap_surface`            | Fibrous, grooves, scaly, smooth                        |
| `cap_color`              | Brown, red, white, etc.                                |
| `bruises`                | Yes or No                                              |
| `odor`                   | Almond, anise, foul, none, pungent, etc.              |
| `gill_attachment`        | Attached, free, notched                                |
| `gill_spacing`           | Close, crowded                                         |
| `gill_size`              | Broad, narrow                                          |
| `gill_color`             | Black, brown, gray, etc.                               |
| `stalk_shape`            | Enlarging, tapering                                    |
| `stalk_root`             | Bulbous, club, missing, etc.                           |
| `stalk_surface_above_ring` | Fibrous, scaly, silky, smooth                        |
| `stalk_color_above_ring` | Brown, pink, white, etc.                               |
| `veil_type`              | Partial, universal                                     |
| `veil_color`             | Brown, orange, white, yellow                           |
| `ring_number`            | None, one, two                                         |
| `ring_type`              | Cobwebby, large, pendant, etc.                         |
| `spore_print_color`      | Black, chocolate, white, yellow, etc.                  |
| `population`             | Abundant, clustered, scattered, etc.                   |
| `habitat`                | Grasses, leaves, meadows, woods, etc.                 |
| `stalk_height`           | Numerical                                              |
| `cap_diameter`           | Numerical                                              |
| `Unnamed: 0`             | Index column (dropped)                                 |

---

## 📂 Files in This Repository

| File Name               | Description                                               |
|-------------------------|-----------------------------------------------------------|
| `mushroom.csv`          | Main dataset                                              |
| `Support Vector mechine.docx` | Assignment instructions                             |
| `SVM.ipynb`             | Jupyter Notebook with full implementation and analysis    |

---

## 🛠️ Tools and Libraries Used

- **pandas**, **numpy** – Data manipulation
- **sklearn.model_selection** – `train_test_split`, `GridSearchCV`
- **sklearn.preprocessing** – `LabelEncoder`, `StandardScaler`
- **sklearn.svm** – `SVC` for SVM implementation
- **sklearn.metrics** – `confusion_matrix`, `classification_report`
- **matplotlib**, **seaborn** – Visualization

---

## 📊 Project Workflow

### 📌 Task 1: Exploratory Data Analysis (EDA)

- Loaded and inspected dataset
- Verified data size: 2000 entries, 26 columns
- Dropped `Unnamed: 0` column
- No missing values found
- Visualized distributions of `stalk_height` and `cap_diameter`
- Used bar plots for categorical feature distributions

---

### 📌 Task 2: Data Preprocessing

- **Label Encoding** for categorical columns
- **Feature Scaling** using `StandardScaler`
- Split dataset into:
  - `X`: Features
  - `y`: Target (`class`)
- **Train/Test Split**: 80% training, 20% testing

---

### 📌 Task 3: Data Visualization

- **Target Distribution**:
  - Dataset is fairly balanced
- **Feature Relationships**:
  - Used scatter plots (with hue by class) for numerical features
  - Visualized patterns of separation (some features show clustering by class)

---

### 📌 Task 4: SVM Baseline Model

- Implemented **SVC** with `linear` kernel
- Evaluated using:
  - `confusion_matrix`
  - `classification_report` (accuracy, precision, recall, F1-score)

---

### 📌 Task 5: SVM Visualization (Optional)

- Not explicitly implemented, but typically done via **PCA** for decision boundary visualization in 2D
- Useful for understanding model behavior in reduced dimensions

---

### 📌 Task 6: Hyperparameter Tuning with GridSearchCV

- Parameters tuned:
  - `kernel`: `linear`, `rbf`, `poly`
  - `C`: 0.1, 1, 10, 100
  - `gamma`: `scale`, `auto`
- Used `GridSearchCV` for optimal combination
- Re-trained model with best parameters
- Improved **accuracy and F1-score** observed

---

### 📌 Task 7: Kernel Comparison and Final Evaluation

| Kernel | Characteristics | Notes |
|--------|-----------------|-------|
| `linear` | Fast, works on linearly separable data | Good baseline |
| `rbf`    | Maps to high-dimensional space | Often best performance |
| `poly`   | Captures interactions between features | Slightly slower |

Best performance typically from `RBF` kernel.

---

## ✅ Strengths & Weaknesses of SVM

### ✅ Strengths

- Handles **high-dimensional** data well
- Robust with **non-linear kernels**
- Effective for **binary classification**
- Good with **small- to medium-sized datasets**

### ❌ Weaknesses

- Sensitive to **feature scaling**
- Performance depends on **kernel and parameter tuning**
- Less interpretable ("black-box")
- Slower on **very large datasets**

---

## 🔎 Real-World Applications of SVM

- **Image Classification**: Face detection, handwriting recognition
- **Text Mining**: Spam filtering, sentiment analysis
- **Bioinformatics**: Protein classification, disease detection
- **Finance**: Fraud detection, credit scoring
- **Remote Sensing**: Satellite image classification

---

## ▶️ How to Run This Project

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/mushroom-svm.git
   cd mushroom-svm
   ```

2. **Install Dependencies**
   ```bash
   pip install pandas numpy scikit-learn matplotlib seaborn
   ```

3. **Open Jupyter Notebook**
   ```bash
   jupyter notebook
   ```

4. **Run the Code**
   - Open `SVM.ipynb`
   - Run all cells to view EDA, preprocessing, training, and evaluation

---

## 📌 Summary

This project demonstrates how to apply Support Vector Machines (SVM) to a real-world binary classification task. With careful **preprocessing**, **tuning**, and **evaluation**, SVM proves to be a **powerful and accurate** tool for classifying mushroom edibility. This implementation serves as a strong foundation for similar classification challenges.

---
