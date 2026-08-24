# 🧬 AIDS Virus Infection Prediction using Machine Learning

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](https://jupyter.org/)
[![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Machine%20Learning-F7931E.svg)](https://scikit-learn.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

An end-to-end Machine Learning solution designed to predict AIDS virus infection status based on healthcare statistics, patient demographics, laboratory results, and clinical treatment histories.

---

## 📌 Table of Contents
- [Project Overview](#-project-overview)
- [How It Is Useful](#-how-it-is-useful)
- [Dataset Architecture & Attributes](#-dataset-architecture--attributes)
- [What the Project Does](#-what-the-project-does)
- [Machine Learning Models & Algorithms Used](#-machine-learning-models--algorithms-used)
- [Technologies Used & Detailed Breakdown](#-technologies-used--detailed-breakdown)
- [Repository Structure](#-repository-structure)
- [Installation & Quick Start](#-installation--quick-start)
- [License](#-license)

---

## 🎯 Project Overview

Early diagnosis and risk stratification play vital roles in managing the Human Immunodeficiency Virus (HIV) and preventing its progression to Acquired Immunodeficiency Syndrome (AIDS). 

This project utilizes historical medical statistics initially published in 1996 to build an automated classification workflow. By leveraging clinical indicators and patient attributes, the machine learning models predict infection risk accurately to support predictive modeling and healthcare analytics.

---

## 💡 How It Is Useful

- **Predictive Risk Modeling:** Predicts AIDS virus infection probability based on key physiological markers and treatment background.
- **Exploratory Data Analysis (EDA):** Uncovers critical relationships between attributes (such as CD4/CD8 cell counts, Karnofsky scores, and antiretroviral history) and infection outcomes.
- **Healthcare & Epidemiological Research:** Serves as a valuable clinical research resource for evaluating treatment efficacy and disease progression patterns.
- **Data-Driven Diagnostics:** Replaces manual intuition with data-driven predictions derived from medical indicators to minimize human error.

---

## 📊 Dataset Architecture & Attributes

The dataset comprises demographic, clinical, treatment, and laboratory attributes:

| Attribute | Data Type / Representation | Description |
| :--- | :--- | :--- |
| `time` | Numerical | Time to failure or censoring |
| `trt` | Categorical | Treatment indicator (`0` = ZDV only, `1` = ZDV + ddI, `2` = ZDV + Zal, `3` = ddI only) |
| `age` | Numerical | Age (in years) at baseline |
| `wtkg` | Numerical | Weight (in kg) at baseline |
| `hemo` | Binary | Hemophilia status (`0` = No, `1` = Yes) |
| `homo` | Binary | Homosexual activity status (`0` = No, `1` = Yes) |
| `drugs` | Binary | History of IV drug use (`0` = No, `1` = Yes) |
| `karnof` | Numerical | Karnofsky performance score (scale `0–100`) |
| `oprior` | Binary | Non-ZDV antiretroviral therapy pre-175 (`0` = No, `1` = Yes) |
| `z30` | Binary | ZDV usage in the 30 days prior to 175 (`0` = No, `1` = Yes) |
| `preanti` | Numerical | Days pre-175 antiretroviral therapy |
| `race` | Binary | Race classification (`0` = White, `1` = Non-white) |
| `gender` | Binary | Gender identification (`0` = Female, `1` = Male) |
| `str2` | Binary | Antiretroviral history (`0` = Naive, `1` = Experienced) |
| `strat` | Categorical | Antiretroviral history stratification (`1` = Naive, `2` = >1 & <=52 weeks, `3` = >52 weeks) |
| `symptom` | Binary | Symptomatic indicator (`0` = Asymptomatic, `1` = Symptomatic) |
| `treat` | Binary | Treatment classification (`0` = ZDV only, `1` = Others) |
| `offtrt` | Binary | Indicator of off-treatment before 96±5 weeks (`0` = No, `1` = Yes) |
| `cd40` | Numerical | Baseline CD4 T-cell count |
| `cd420` | Numerical | CD4 T-cell count at 20±5 weeks |
| `cd80` | Numerical | Baseline CD8 T-cell count |
| `cd820` | Numerical | CD8 T-cell count at 20±5 weeks |
| `infected` | Binary (**Target**) | Target variable: AIDS virus infection status (`0` = No, `1` = Yes) |

---

## 🔍 What the Project Does

1. **Data Preprocessing & Cleaning:** Handles missing data, formats features, scales continuous numerical markers (like CD4/CD8 counts), and encodes categorical health parameters.
2. **Exploratory Data Analysis (EDA):** Visualizes feature distributions, analyzes statistical correlations, and evaluates how demographics and lab measurements affect infection outcomes.
3. **Model Training & Benchmarking:** Trains supervised machine learning algorithms to identify the optimal model for AIDS infection prediction.
4. **Model Performance Evaluation:** Measures predictive accuracy through Precision, Recall, F1-Score, Confusion Matrices, and ROC-AUC curves.

---

## 🤖 Machine Learning Models & Algorithms Used

The primary notebook (`final.ipynb`) trains and evaluates multiple classification algorithms to compare performance on clinical and lab attributes:

| Model / Algorithm | Type | Role & Description |
| :--- | :--- | :--- |
| **Logistic Regression** | Linear Classification | Estimates infection risk probabilities using linear boundaries; serves as an interpretable baseline model. |
| **Random Forest Classifier** | Ensemble Learning | Combines multiple decision trees to model complex non-linear interactions between lab values (e.g., CD4 counts) and health history. |
| **Support Vector Machine (SVM)** | Kernel Classifier | Maps patient attributes into higher-dimensional space to find the optimal hyperplane separating infected vs. non-infected cases. |
| **Decision Tree Classifier** | Tree-based Model | Constructs intuitive rule-based pathways to categorize patient infection risk based on clinical thresholds. |
| **K-Nearest Neighbors (KNN)** | Instance-based | Predicts infection status by assessing the clinical profile similarity of the nearest historical patient records. |
| **Gradient Boosting / XGBoost** | Sequential Boosting | Optimizes predictive accuracy sequentially by reducing classification errors from previous decision trees. |

---

## 🛠️ Technologies Used & Detailed Breakdown

| Technology | Role | Detailed Explanation |
| :--- | :--- | :--- |
| **Python** | Core Language | Provides the foundation for building data pipelines, script automation, and analytical workflows. |
| **Pandas** | Data Processing | Loads medical datasets, cleans null values, handles tabular data manipulation, and performs feature transformations. |
| **NumPy** | Scientific Computing | Executes vector operations, fast matrix math, and numerical calculations required by ML algorithms. |
| **Matplotlib** | Data Visualization | Renders baseline visual graphics, distribution plots, custom charts, and model evaluation curves. |
| **Seaborn** | High-Level Visualization | Builds clean statistical graphics including correlation heatmaps and feature comparison boxplots. |
| **Scikit-Learn** | Machine Learning | Features automated scaling tools, dataset splitting algorithms, classification algorithms, and evaluation metrics. |
| **Jupyter Notebook** | Development Interface | Executable workspace (`final.ipynb`) documenting step-by-step code execution, EDA outputs, and model benchmarks. |

---

## 📂 Repository Structure

```text
AIDS-Virus-Infection-Prediction-using-ml/
├── final.ipynb        # Primary Jupyter Notebook containing data preprocessing, EDA, and ML models
└── README.md          # Full project documentation
```

---

## ⚙️ Installation & Quick Start

### Prerequisites
Ensure **Python 3.8+** is installed on your machine.

### 1. Clone the Repository
```bash
git clone https://github.com/abdoha00/AIDS-Virus-Infection-Prediction-using-ml.git
cd AIDS-Virus-Infection-Prediction-using-ml
```

### 2. Create a Virtual Environment (Optional)
```bash
# Windows
python -m venv venv
venv\Scripts\activate

# macOS / Linux
python -m venv venv
source venv/bin/activate
```

### 3. Install Required Dependencies
```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

### 4. Run the Notebook
```bash
jupyter notebook final.ipynb
```

---

## 📜 License

Distributed under the MIT License. See `LICENSE` for more information.
