# Medical Data Visualizer

This project analyzes and visualizes medical examination data to explore the relationship between cardiovascular disease and various health and lifestyle factors. It uses Python with **Pandas**, **Seaborn**, **Matplotlib**, and **NumPy**.

---

## 📁 Dataset

File: `medical_examination.csv`

Each row = one patient  
Each column = examination result or lifestyle factor

### Columns

| Column         | Description                                      |
|----------------|--------------------------------------------------|
| `age`          | Age in days                                      |
| `height`       | Height in cm                                     |
| `weight`       | Weight in kg                                     |
| `ap_hi`        | Systolic blood pressure                          |
| `ap_lo`        | Diastolic blood pressure                         |
| `cholesterol`  | 1: normal, 2: above normal, 3: well above normal |
| `gluc`         | 1: normal, 2: above normal, 3: well above normal |
| `smoke`        | 0: No, 1: Yes                                    |
| `alco`         | 0: No, 1: Yes                                    |
| `active`       | 0: No, 1: Yes                                    |
| `cardio`       | 0: No cardiovascular disease, 1: Has disease     |

---

## 🧮 Processing & Features

- **BMI & Overweight:**  
  A new column `overweight` is added:   
  If BMI > 25, set `overweight = 1`; else `0`.

- **Normalization of values:**
  - `cholesterol` & `gluc` → convert:  
    - 1 → 0 (good)  
    - 2 or 3 → 1 (bad)

---

## 📊 Visualizations

### 1. Categorical Plot

- Shows count of good/bad values for:
  - `cholesterol`, `gluc`, `smoke`, `alco`, `active`, `overweight`
- Split by cardiovascular disease (`cardio = 0` or `1`)

📁 Output: `catplot.png`

### 2. Heatmap

- Cleans data:
  - Diastolic ≤ Systolic
  - Height and weight within 2.5–97.5 percentile
- Correlation matrix visualized

📁 Output: `heatmap.png`

---

## 🛠️ Code

Python
