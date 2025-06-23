
````markdown
# 🏡 Home Price Prediction using Linear Regression

This project demonstrates how to use **Linear Regression** for predicting home prices based on area and location. It covers **manual one-hot encoding** using pandas as well as **automated encoding** using `sklearn`'s `ColumnTransformer`.

---

## 📊 Dataset

The dataset `homeprices.csv` contains:
- `town`: Town name (categorical)
- `area`: Area of the house (in sq ft)
- `price`: Target price to predict

---

## 📦 Libraries Used

- pandas
- scikit-learn
- numpy (implicitly used via sklearn)

---

## 🚀 How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/home-price-prediction.git
   cd home-price-prediction
````

2. Open the notebook or run the script:

   ```bash
   jupyter notebook HomePricePrediction.ipynb
   ```

3. Or use the Python script:

   ```bash
   python home_price_predictor.py
   ```

---

## 🔍 What’s Inside

### ✔️ Method 1: Manual Encoding with pandas

* Load dataset with pandas
* Create dummy variables using `pd.get_dummies()`
* Train `LinearRegression` model on the modified data
* Predict prices for new homes in different towns

### ✔️ Method 2: Label + OneHot Encoding with scikit-learn

* Encode `town` using `LabelEncoder` and `OneHotEncoder`
* Use `ColumnTransformer` to manage transformations cleanly
* Drop one dummy variable to avoid dummy variable trap
* Predict prices using encoded input

---

## 🧠 Model Used

* **LinearRegression** from `sklearn.linear_model`
* Trained on one-hot encoded features
* Accuracy is evaluated using `.score()`

---

## 🎯 Sample Predictions

```python
model.predict([[3400, 0, 0]])  # 3400 sq ft home in west windsor
model.predict([[2800, 0, 1]])  # 2800 sq ft home in robbinsville
```

Using ColumnTransformer:

```python
model.predict([[0, 1, 3400]])  # west windsor
model.predict([[1, 0, 2800]])  # robbinsville
```

---

## ✅ Result

* Linear regression gives a reliable estimate of home prices based on area and location.
* Demonstrates both basic and scalable encoding approaches for categorical data.

---

## 🤝 Contributing

Pull requests are welcome! Please open an issue to discuss changes or enhancements before submitting.

---

## 📜 License

[MIT License](LICENSE)

---


