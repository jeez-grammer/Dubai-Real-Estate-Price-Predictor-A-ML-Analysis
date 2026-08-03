# 🇦🇪 Dubai Real Estate Rental Price Predictor

## 📍 Project Overview
This project implements a machine learning pipeline to predict annual rental prices for properties across the UAE (Dubai and Abu Dhabi). By analyzing property features and locations, the model provides a data-driven estimate of market rental values.

### 🎯 Business Goal
The objective is to transition from descriptive analytics to **predictive analytics**. This tool allows property owners and agents to determine fair market value based on real-world data, reducing the risk of underpricing or overpricing properties.

---

## 🤖 Technical Pipeline

### 1. Data Cleaning & Preprocessing
To ensure high model accuracy and prevent bias, the following preprocessing steps were implemented:
*   **Outlier Removal:** Identified and removed extreme outliers (including zero-rent entries and ultra-luxury anomalies) using quantile-based filtering.
*   **Feature Engineering:**
    *   **One-Hot Encoding:** Converted categorical variables (`Property Type`, `Furnishing`, `City`, `Location`) into numerical formats.
    *   **Feature Scaling:** Utilized `StandardScaler` to normalize numerical features (Beds, Baths, Area), ensuring the model treats all features with equal importance.

<img width="862" height="548" alt="Screenshot 2026-07-28 at 2 17 23 PM" src="https://github.com/user-attachments/assets/9b1b986f-210b-42d1-b6fb-347da2d01bca" />

### 2. Model Development & Evaluation
I compared a baseline model against a high-performance ensemble model to determine the best predictive approach:

*   **Linear Regression (Baseline):** Used to establish a benchmark for linear relationships.
*   **Random Forest Regressor (Advanced):** Used to capture complex, non-linear interactions between property features and location.

**Performance Comparison:**
| Model | Mean Absolute Error (MAE) | R-squared Score ($R^2$) |
| :--- | :--- | :--- |
| Linear Regression | ~39,911 AED | 0.7085 |
| **Random Forest** | **~19,796 AED** | **0.8867** |

**Key Result:** The Random Forest model significantly outperformed the baseline, explaining nearly **89% of the variance** in rental prices.

<img width="860" height="548" alt="Screenshot 2026-07-28 at 2 19 28 PM" src="https://github.com/user-attachments/assets/40c21886-7fab-4c05-8864-849a0a3771b0" />

---

## 🚀 Prediction Capability
The project includes a production-ready prediction function. By inputting property specifications, the model outputs an estimated annual rent.

**Example Prediction:**
*   **Input:** 2 Beds, 2 Baths, 1200 sqft, Apartment, Furnished, Abu Dhabi, Yas Island.
*   **Predicted Rent:** `~100,421 AED`

---

## 📂 Repository Structure
```text
├── data/
│ └── dubai_properties.csv # full dataset
├── dubai_prop.ipynb # Full EDA, Cleaning, and ML Pipeline
├── requirements.txt # List of Python dependencies
```

## ⚙️ Installation & Setup
To run this project locally:

**1. Clone the repository** 
```bash
git clone https://github.com/jeez-grammer/Dubai-Real-Estate-Price-Predictor-A-ML-Analysis.git
```
**2. Install dependencies** 
```bash
pip install -r requirements.txt
```
**3. Launch the notebook**
```bash
jupyter notebook dubai_prop.ipynb or open dubai_prop.ipynb to just copy and paste the codes in each cell.
```

---

**Developed by Nelson Viernes**  
*Data Administrator*
