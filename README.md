# 🚢 Titanic Survival Prediction – Data Cleaning & Preprocessing

A comprehensive data cleaning, exploratory data analysis (EDA), and feature engineering project using the classic **Titanic: Machine Learning from Disaster** dataset from Kaggle.

---

## 📌 Project Overview

Data cleaning and preprocessing are foundational steps before training machine learning models. Real-world tabular datasets frequently contain missing values, skewed distributions, noisy attributes, and categorical features that require encoding.

This project demonstrates a systematic, step-by-step pipeline to clean and transform the raw Titanic dataset into a clean, ready-to-model dataset.

---

## 🌟 Key Highlights & Methodology

1. **Exploratory Data Analysis (EDA):**
   - Structural inspection using `.info()`, `.describe()`, and `.shape`.
   - Identification of categorical vs. numerical features.
   - Examination of distributions, cardinality, and summary statistics.

2. **Missing Data Handling:**
   - Detailed missing value analysis (`Missing count` & `Percentage`).
   - **`Age` Imputation:** Imputed using **Median** (robust against right-skewed age distribution compared to Mean).
   - **`Embarked` Imputation:** Filled missing records with the most frequent category (**Mode** `'S'`).
   - Handled high-cardinality/missing cabin records responsibly.

3. **Categorical Feature Encoding:**
   - **`LabelEncoder`:** Converted binary features (`Sex`) into ordinal/integer representations.
   - **`OneHotEncoder`:** One-hot encoded nominal categorical features (`Sex`, `Embarked`) to prevent artificial ordinal hierarchy.

4. **Data Visualizations:**
   - Distribution comparisons for `Age` **before vs. after** imputation to ensure the data distribution is preserved without introducing distortion.
   - Survival breakdown visualizations across passenger demographics.

5. **Cleaned Dataset Export:**
   - Verified that total missing values are resolved.
   - Exported the final processed dataset to `titanic_cleaned.csv`.

---

## 📁 Repository Structure

```
Titanic-Data-Cleaning/
├── Titanic_Data_Cleaning.ipynb    # Main Jupyter Notebook containing the full workflow
├── Titanic-Dataset.csv            # Original Kaggle Titanic dataset
├── requirements.txt               # Required Python packages
├── .gitignore                     # Git ignore rules for checkpoints & temp files
└── README.md                      # Project documentation
```

---

## 🚀 Getting Started

### Prerequisites

Ensure you have Python 3.8+ installed.

### Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/vignesh124-ai/Titanic-Data-Cleaning.git
   cd Titanic-Data-Cleaning
   ```

2. Create and activate a virtual environment (optional but recommended):
   ```bash
   python -m venv venv
   # On Windows:
   venv\Scripts\activate
   # On macOS/Linux:
   source venv/bin/activate
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

### Running the Notebook

Launch Jupyter Notebook or Jupyter Lab:
```bash
jupyter notebook Titanic_Data_Cleaning.ipynb
```

---

## 📊 Summary of Data Transformations

| Feature | Original Type | Missing Values Handled | Transformation Applied |
| :--- | :--- | :--- | :--- |
| **`Age`** | Float64 | ~19.86% missing | Median imputation |
| **`Embarked`** | Object | 2 missing records | Mode imputation (`'S'`) + One-Hot Encoding |
| **`Sex`** | Object | 0 missing | Label Encoding & One-Hot Encoding |
| **`Fare`** | Float64 | 0 missing | Verified distribution |
| **`Survived`** | Int64 | 0 missing | Target variable |

---

## 👤 Author

- **Bhuma Vignesh**
- GitHub: [@vignesh124-ai](https://github.com/vignesh124-ai)
