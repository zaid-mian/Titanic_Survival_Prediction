# 🚢 Titanic Survival – EDA & Decision-Tree Baseline

**Minimal yet complete** walk-through of the Titanic dataset:  
exploratory data analysis → preprocessing → Decision-Tree modelling → evaluation.

---

## 📦 Quick Start

1. **Download** the classic Titanic dataset:  
   - [Kaggle Titanic Data](https://www.kaggle.com/c/titanic/data) *(requires free Kaggle login)*  
   - [OpenML Titanic CSV](https://www.openml.org/data/get_csv/16826755/phpMYEkMl) *(direct download)*  

   already present in folder just downalod it `titanic.csv` in this project folder.  

2. **Install** requirements:

   ```bash
   pip install -r requirements.txt
   ```

3. **Run** the notebook or the script:

   ```bash
   python titanic_eda_dt.py
   ```

---

## 📁 Repository Contents

| File               | Purpose                                     |
|--------------------|---------------------------------------------|
| `titanic_eda_dt.py` | Complete runnable script (Python ≥ 3.8)     |
| `requirements.txt`  | pandas, seaborn, scikit-learn, matplotlib   |
| `README.md`         | This file                                   |

---

## 📊 What You’ll See

**Console output**
- Dataset shape  
- Missing-value audit  
- Target class balance  
- Accuracy & classification report  

**Plots**
- Survival counts  
- Survival by Sex  
- Age & Fare distributions  
- Correlation heat-map  
- Confusion matrix  

---

## 🔧 Pipeline Details

| Step            | Tool                  | Notes                                                |
|-----------------|-----------------------|------------------------------------------------------|
| Missing values  | `SimpleImputer`       | median (numeric), most-frequent (categorical)        |
| Encoding        | `OneHotEncoder`       | Sex, Embarked, Pclass                                |
| Scaling         | `MinMaxScaler`        | Numeric features → 0–1 range                         |
| Model           | `DecisionTreeClassifier` | `random_state=42`                                |
| Split           | `train_test_split`    | 80/20 stratified split                               |

👉 Typical baseline accuracy ≈ **78%**

---

## 🧪 Extend / Reuse

- Swap in other estimators (RandomForest, XGBoost) with one-line change.  
- Tune hyperparameters via `GridSearchCV`.  
- Export pipeline with `joblib` for downstream inference.  

---

## 📄 License

MIT – use freely.
