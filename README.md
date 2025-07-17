# Linear-Logistic-Regression
````
# 📊 Beginner Machine Learning with Scikit-learn

This project contains simple examples of two foundational machine learning models using Python and Scikit-learn:

1. **Linear Regression** – For predicting continuous values (like house price).
2. **Logistic Regression** – For predicting binary values (like pass/fail).

---

## 🧠 What You'll Learn

- The difference between Linear and Logistic Regression
- How to train models using simple datasets
- How to make predictions with `.predict()` and `.predict_proba()`
- Understanding the output and what it means

---

## 📈 1. Linear Regression – House Price Prediction

### ✅ Problem:
> Predict the **price** of a house based on its **square footage**.

### 📘 Sample Dataset:

| Square Feet | Price (₹ Lakhs) |
|-------------|------------------|
| 500         | 5                |
| 750         | 7                |
| 1000        | 10               |
| 1200        | 12               |

### 🔧 Python Code:

```
from sklearn.linear_model import LinearRegression

# Input (X): Square feet
# Output (y): Price in Lakhs
X = [[500], [750], [1000], [1200]]
y = [5, 7, 10, 12]

# Train the model
model = LinearRegression()
model.fit(X, y)

# Predict price of 900 sq.ft
prediction = model.predict([[900]])
print("Predicted Price:", prediction[0], "Lakhs")
````

### 💡 Output Example:

```
Predicted Price: 9.0 Lakhs
```

---

## 🔁 2. Logistic Regression – Pass/Fail Prediction

### ✅ Problem:

> Predict whether a student will **pass or fail** based on how many **hours they studied**.

### 📘 Sample Dataset:

| Hours Studied | Result   |
| ------------- | -------- |
| 1             | 0 (Fail) |
| 2             | 0 (Fail) |
| 3             | 0 (Fail) |
| 4             | 1 (Pass) |
| 5             | 1 (Pass) |
| 6             | 1 (Pass) |

### 🔧 Python Code:

```
from sklearn.linear_model import LogisticRegression

# Input (X): Hours studied
# Output (y): 1 = Pass, 0 = Fail
X = [[1], [2], [3], [4], [5], [6]]
y = [0, 0, 0, 1, 1, 1]

# Train the model
model = LogisticRegression()
model.fit(X, y)

# Predict result for 3.5 hours of study
probability = model.predict_proba([[3.5]])
prediction = model.predict([[3.5]])

print("Probability of passing:", probability[0][1])
print("Prediction (1=pass, 0=fail):", prediction[0])
```

### 💡 Output Example:

```
Probability of passing: 0.72
Prediction (1=pass, 0=fail): 1
```

---

## 📦 Requirements

* Python 3.x
* Scikit-learn
* Jupyter Notebook or any Python IDE

### 🛠 Install Required Library

```
pip install scikit-learn
```

---

## 📚 Folder Structure

```
📁 your-project-folder/
├── linear_regression.py
├── logistic_regression.py
└── README.md
```

---

## 🙌 About

These mini-projects are perfect for beginners who want to understand how machine learning models work using Scikit-learn. Feel free to fork, modify, or contribute!

---

## 📬 Contact

If you have any questions or suggestions, feel free to open an issue or reach out.

Happy Learning! 🚀

