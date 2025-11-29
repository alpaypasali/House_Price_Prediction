# 🏡 **House Prices — Advanced Regression Techniques**
### 🎯 *End-to-End Machine Learning Pipeline (Kaggle Competition)*

This project is an end-to-end regression pipeline built using the **Kaggle House Prices: Advanced Regression Techniques** dataset.  
The goal is to develop a machine learning system that predicts the **SalePrice** of a home as accurately as possible based on its physical and qualitative features.

---

## 📂 **Dataset Story**

This project uses the well-known **Ames Housing Dataset**, consisting of:

- **79 explanatory variables**
- **1 target variable (SalePrice)**
- **1,460 observations in the training set**
- **1,459 observations in the test set**

The dataset includes a wide range of information—physical attributes, renovation status, material quality, location, and overall house condition.

---

## 🧭 **Roadmap of the Project**

### **1️⃣ Exploratory Data Analysis (EDA)**  
- Numerical & categorical feature distributions  
- Correlation analysis with SalePrice  
- Missing value inspection  
- Pairplots, heatmaps, boxplots  

### **2️⃣ Feature Engineering**  
- Missing value imputation (median, mode, custom flags)  
- Rare category handling  
- Outlier detection using IQR  
- New feature creation:
  - `TotalSF`
  - Age-related features (HouseAge, RemodelAge)
  - Quality × Area interactions  

### **3️⃣ Preprocessing**  
- Label Encoding & One-Hot Encoding  
- Scaling (StandardScaler)  
- Train/Test split  

### **4️⃣ Modeling**  
Models trained and evaluated:

- **LightGBM**
- **Random Forest**
- **XGBoost**
- **GradientBoostingRegressor**
- **Linear Models** (Ridge / Lasso / ElasticNet)

### **5️⃣ Hyperparameter Optimization**  
- GridSearchCV  
- RandomizedSearchCV  
- 5-Fold Cross-Validation  
- RMSE-based scoring  

### **6️⃣ Model Evaluation**  
- Train/Test RMSE  
- Cross-validation RMSE  
- Residual plots  
- Feature importance visualizations  

---

## ⚠️ **About Warnings**

During execution, you may encounter warnings such as:



This typically occurs when Seaborn attempts to compute a mean on an empty subset of data (e.g., when a category has no observations after filtering).

Additional warnings suppressed for cleaner output:

warnings.simplefilter(action='ignore', category=FutureWarning)
warnings.simplefilter("ignore", category=ConvergenceWarning)


These do not affect model performance.

🧠 Technologies & Skills Used

Python

Pandas, NumPy

Seaborn, Matplotlib

Scikit-Learn

LightGBM, XGBoost

Feature Engineering

Hyperparameter Tuning

Cross-Validation

Regression Metrics: RMSE, MAE, R²

🗂️ Project Structure
house-price-regression/
│── README.md
│── notebook.ipynb
│── data/
│     ├── train.csv
│     ├── test.csv
│── models/
│── utils/


📊 Model Performance

The best performance was typically achieved using LightGBM with optimized hyperparameters.

CV RMSE: ~0.12 – 0.13

Test RMSE: Competitive Kaggle leaderboard score
(Exact value varies depending on feature engineering & tuning.)

🚀 How to Run the Project
git clone https://github.com/<username>/house-price-regression.git
cd house-price-regression
pip install -r requirements.txt
jupyter notebook

