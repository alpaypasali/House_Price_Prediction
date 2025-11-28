🏡 House Prices — Advanced Regression Techniques
🎯 End-to-End Machine Learning Pipeline (Kaggle Competition)

Bu proje, Kaggle House Prices: Advanced Regression Techniques veri seti kullanılarak geliştirilmiş uçtan uca bir regresyon projesidir.
Amaç, bir kişinin hayalindeki evin özelliklerine göre tahmini satış fiyatını en doğru şekilde öngören bir ML sistemi oluşturmaktır.

📂 Dataset Story

Bu çalışma, Ames, Iowa şehrindeki evlere ait 79 açıklayıcı özellik ve SalePrice hedef değişkeninden oluşan Kaggle veri setini kullanır.

Train set: 1,460 gözlem

Test set: 1,459 gözlem

Veri seti; evin fiziksel özelliklerinden, lokasyon bilgisine, malzeme kalitesinden tamirat durumuna kadar geniş bir yelpazede detay içerir.

🧭 Roadmap of the Project
1️⃣ Exploratory Data Analysis (EDA)

✔ Numerik ve kategorik değişkenlerin dağılımları
✔ SalePrice ile korelasyon analizi
✔ Eksik değerlerin incelenmesi
✔ İlişkisel grafikler (pairplot, heatmap, boxplot)

2️⃣ Feature Engineering

✔ Eksik değer doldurma (median, mode, special flag)
✔ Rare encoding
✔ Outlier yakalama – IQR bazlı
✔ Yeni değişken üretimi (TotalSF, age features, quality × area interactions)

3️⃣ Preprocessing

✔ Label Encoding & One-Hot Encoding
✔ Scaling (StandardScaler)
✔ Train / Test split

4️⃣ Modeling

✔ LightGBM
✔ Random Forest
✔ XGBoost
✔ GradientBoostingRegressor
✔ Linear Models (Ridge / Lasso / ElasticNet)

5️⃣ Hyperparameter Optimization

✔ GridSearchCV
✔ RandomizedSearchCV
✔ Cross-validation (k=5)
✔ RMSE odaklı skor optimizasyonu

6️⃣ Model Evaluation

✔ Train-Test RMSE
✔ CV RMSE
✔ Residual plots
✔ Feature importance grafikleri

⚠️ Warnings Hakkında Not

Notebook çalışırken zaman zaman aşağıdaki uyarılar oluşabilir:

/usr/local/lib/python3.11/dist-packages/seaborn/algorithms.py:98: RuntimeWarning: Mean of empty slice


Neden gelir?

Boş bir seri üzerinden ortalama alınmaya çalışıldığında oluşur.

Örneğin bir kategorinin alt grubunda hiç gözlem yoksa seaborn bunu raporlar.
Çözüm: Veri filtrelerini ve null değerleri kontrol ettim; model performansını etkilemediği için ignore edilmiştir.

Ayrıca:

warnings.simplefilter(action='ignore', category=FutureWarning)
warnings.simplefilter("ignore", category=ConvergenceWarning)


Model eğitim sürecinde gereksiz uyarı kalabalığını önlemek için eklenmiştir.

🧠 Used Technologies & Skills

Python

Pandas, NumPy

Seaborn, Matplotlib

Scikit-Learn

LightGBM, XGBoost

Feature Engineering

Hyperparameter Tuning

Cross-Validation

Regression Metrics (RMSE, MAE, R²)

🗂️ Project Structure
📁 house-price-regression/
│── 📄 README.md
│── 📓 notebook.ipynb
│── 📁 data/
│     ├── train.csv
│     ├── test.csv
│── 📁 models/
│── 📁 utils/

📊 Model Performance

En yüksek performans genellikle LightGBM + optimized parameters ile alınmıştır.

CV RMSE: 0.12–0.13 aralığı

Test set RMSE: Highly competitive Kaggle score

(Not: Tam skor notebook içeriğine göre güncellenecektir.)

🚀 How to Run the Project
git clone https://github.com/<username>/house-price-regression.git
cd house-price-regression
pip install -r requirements.txt
jupyter notebook
