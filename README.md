# Iris Classification using XGBoost

This project uses the **Iris dataset** from `sklearn.datasets` to classify flowers into **Setosa, Versicolor, and Virginica** using **XGBoost**. The model achieves **100% accuracy** with the chosen hyperparameters.

## 📊 Dataset
- Source: `from sklearn.datasets import load_iris`
- Samples: 150
- Features: 4 numeric features
  - Sepal length
  - Sepal width
  - Petal length
  - Petal width
- Target: 3 classes
  - 0 → Setosa
  - 1 → Versicolor
  - 2 → Virginica

## 🛠️ Tech Stack
- Python
- Pandas, NumPy (data handling)
- Scikit-learn (train/test split, metrics, classification report)
- XGBoost (model training)

## ⚙️ Model Parameters
```python
model = XGBClassifier(
    n_estimators=100,
    max_depth=6,
    subsample=0.8,
    colsample_bytree=0.8,
    booster='dart',
    eval_metric='rmse',
    random_state=42,
    objective='multi:softprob',
    reg_alpha=1.0
)
📈 Results

Accuracy: 100%

Confusion Matrix:

[[10,  0,  0],
 [ 0,  9,  0],
 [ 0,  0, 11]]


Classification Report:

Class	Precision	Recall	F1-score	Support
0 (Setosa)	1.00	1.00	1.00	10
1 (Versicolor)	1.00	1.00	1.00	9
2 (Virginica)	1.00	1.00	1.00	11
Accuracy			1.00	30
🚀 How to Run
# Clone the repository
git clone https://github.com/ishanegi5/iris-classification-xgboost.git
cd iris-classification-xgboost

# Install dependencies
pip install -r requirements.txt

# Run the notebook or script
jupyter notebook Iris_XGBoost.ipynb

📌 Requirements
pandas
numpy
scikit-learn
xgboost
matplotlib
seaborn

📢 License

This project is open-source and available under the MIT License.

🔗 Author: Isha Negi
