# 🚗 CarPriceML
A beginner-friendly machine learning project created to practice **ML fundamentals, data preprocessing, categorical encoding, train-test splitting, regression models, and basic model evaluation** using a car price prediction dataset.

This project was built primarily as a learning exercise to understand the basic workflow of a machine learning project.

---

## 📌 Project Overview

The project uses a dataset containing information about used cars and their selling prices.

The main objective is to understand how different car-related features can be processed and used to train regression models for predicting the selling price.

The project covers the basic machine learning workflow:

* Loading and exploring data
* Checking dataset shape and information
* Checking missing values
* Encoding categorical features
* Separating features and target
* Splitting data into training and testing sets
* Training regression models
* Evaluating model performance
* Visualizing actual vs predicted values

---

## 📊 Dataset

The dataset contains **301 rows and 9 columns**.

### Features

| Column          | Description               |
| --------------- | ------------------------- |
| `Car_Name`      | Name of the car           |
| `Year`          | Manufacturing year        |
| `Selling_Price` | Selling price of the car  |
| `Present_Price` | Present price of the car  |
| `Kms_Driven`    | Kilometers driven         |
| `Fuel_Type`     | Fuel type of the car      |
| `Seller_Type`   | Type of seller            |
| `Transmission`  | Transmission type         |
| `Owner`         | Number of previous owners |

There are no missing values in the dataset.

---

## 🔄 Data Preprocessing

The categorical columns are converted into numerical values before training the models.

### Fuel Type

```text
Petrol  → 0
Diesel  → 1
CNG     → 2
```

### Seller Type

```text
Dealer      → 0
Individual  → 1
```

### Transmission

```text
Manual      → 0
Automatic   → 1
```

The `Car_Name` column is removed from the input features, while `Selling_Price` is used as the target variable.

---

## 🎯 Features Used

The model uses the following features:

```text
Year
Present_Price
Kms_Driven
Fuel_Type
Seller_Type
Transmission
Owner
```

### Target

```text
Selling_Price
```

---

## ✂️ Train-Test Split

The dataset is divided into training and testing data using `train_test_split`.

```python
X_train, X_test, Y_train, Y_test = train_test_split(
    X,
    Y,
    test_size=0.1,
    random_state=2
)
```

The split uses **90% of the data for training and 10% for testing**.

---

## 🤖 Machine Learning Models

Two basic regression models are explored in this project:

### 1. Linear Regression

```python
from sklearn.linear_model import LinearRegression

lin_reg_model = LinearRegression()
lin_reg_model.fit(X_train, Y_train)
```

**R² Score:**

* Training: `0.8799`
* Testing: `0.8366`

### 2. Lasso Regression

```python
from sklearn.linear_model import Lasso

lass_reg_model = Lasso()
lass_reg_model.fit(X_train, Y_train)
```

**R² Score:**

* Training: `0.8428`
* Testing: `0.8709`

---

## 📈 Model Evaluation

The models are evaluated using the **R² (R-squared) score**.

The project also uses scatter plots to visualize:

```text
Actual Price vs Predicted Price
```

This helps understand how closely the model's predictions are related to the actual selling prices.

---

## 🛠️ Technologies Used

* **Python**
* **Pandas**
* **Matplotlib**
* **Seaborn**
* **Scikit-learn**
* **Jupyter Notebook / Google Colab**

---

## 📚 What I Practiced

This project helped me practice the fundamentals of a typical machine learning workflow:

* Data loading
* Data exploration
* Dataset inspection
* Missing-value checking
* Categorical data encoding
* Feature selection
* Target variable selection
* Train-test splitting
* Linear Regression
* Lasso Regression
* R² score
* Data visualization
* Comparing regression models

---

## 📁 Project Structure

```text
Car-Price-Prediction/
│
├── Car_Price_Prediction.ipynb
├── car data.csv
└── README.md
```

---

## ▶️ How to Run

### Clone the repository

```bash
git clone https://github.com/your-username/Car-Price-Prediction.git
```

### Navigate to the project

```bash
cd Car-Price-Prediction
```

### Install the required libraries

```bash
pip install pandas matplotlib seaborn scikit-learn
```

### Run the notebook

Open `Car_Price_Prediction.ipynb` using **Jupyter Notebook** or **Google Colab** and run the cells sequentially.

---

## 🎯 Purpose of the Project

This project is primarily a **practice project for learning machine learning basics**.

The focus is on understanding the fundamental steps involved in preparing data and building a simple regression model rather than creating a production-ready car price prediction system.

---

## 👨‍💻 Author

**Prawar Karande**

MCA Student | Aspiring Data Scientist / AI-ML Engineer

* GitHub: [prawar-hash](https://github.com/prawar-hash)
* LinkedIn: [Prawar Karande](https://www.linkedin.com/in/prawar-karande-b1ab33249/)
