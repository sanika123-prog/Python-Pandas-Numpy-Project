# 🏠 House Price Prediction & Exploratory Data Analysis

## 📌 Project Overview

This project focuses on **Exploratory Data Analysis (EDA)** and **House Price Prediction** using Python and Machine Learning.

The project analyzes housing data to understand the relationships between different property features and their **SalePrice**. After performing data cleaning, preprocessing, and visualization, machine learning models are trained to predict house prices.

The project also includes an interactive **PriceMeter: Smart House Value** feature that provides a predicted house price using a Linear Regression model.

---

## 🎯 Objectives

* Perform detailed Exploratory Data Analysis on housing data.
* Understand numerical and categorical features.
* Identify and handle missing values.
* Visualize important patterns and distributions.
* Preprocess categorical and numerical features.
* Train machine learning regression models.
* Evaluate model performance using standard regression metrics.
* Create an interactive house price prediction feature.

---

## 🛠️ Technologies & Libraries

The project is developed using Python and the following libraries:

* **Python**
* **Pandas** – Data manipulation and analysis
* **NumPy** – Numerical computations
* **Matplotlib** – Data visualization
* **Seaborn** – Statistical visualization
* **Plotly** – Interactive visualizations
* **Scikit-learn** – Machine learning
* **IPyWidgets** – Interactive PriceMeter interface
* **Jupyter Notebook** – Development environment

---

## 📂 Dataset

The project uses a housing dataset stored as:

```text
train.csv
```

The target variable used for prediction is:

```text
SalePrice
```

The dataset contains both **numerical and categorical housing features**, which are analyzed and processed before model training.

---

## 🔍 Exploratory Data Analysis

The notebook performs several EDA operations, including:

### Dataset Overview

* Dataset information
* Dataset shape
* Statistical summary
* Numerical feature identification
* Categorical feature identification

### Missing Value Analysis

Missing values are identified using:

* Missing value counts
* Missing value percentages

Numerical missing values are handled using the **median**, while categorical missing values are filled with:

```text
None
```

### Data Visualization

The project includes visualizations such as:

* Distribution of `MSZoning`
* Pie charts
* Bar charts
* House sales by month
* Interactive visualizations
* Correlation/heatmap analysis

---

## ⚙️ Data Preprocessing

The following preprocessing steps are performed:

1. Separate the target variable `SalePrice`.
2. Remove `SalePrice` from the feature dataset.
3. Identify numerical and categorical columns.
4. Handle missing values.
5. Convert categorical variables into numerical form using **One-Hot Encoding**.
6. Split the data into training and validation/testing sets.
7. Apply `StandardScaler` to the processed features.

Example:

```python
y = df["SalePrice"]
X = df.drop("SalePrice", axis=1)

X = pd.get_dummies(X, drop_first=True)
```

---

## 🤖 Machine Learning Models

Two regression models are trained in the project.

### 1. Linear Regression

```python
lr_model = LinearRegression()
lr_model.fit(X_train, y_train)
```

Linear Regression is used as a baseline regression model for predicting house prices.

### 2. Random Forest Regressor

```python
rf_model = RandomForestRegressor(
    n_estimators=200,
    random_state=42
)

rf_model.fit(X_train, y_train)
```

The Random Forest model uses multiple decision trees to improve prediction performance.

---

## 📊 Model Evaluation

The trained models are evaluated using the following metrics:

### R² Score

Measures how well the model explains the variation in the target variable.

### MAE – Mean Absolute Error

Measures the average absolute difference between actual and predicted prices.

### MSE – Mean Squared Error

Measures the average squared prediction error.

### RMSE – Root Mean Squared Error

Measures the square root of MSE and provides the error in the same unit as the target variable.

The notebook evaluates both:

* Linear Regression
* Random Forest Regressor

---

## ⭐ PriceMeter: Smart House Value

An interactive **PriceMeter** feature is included in the notebook.

It uses:

```text
Linear Regression
```

to predict a house price and displays the result through an interactive meter.

The interface includes:

* 🏠 Predicted Price Meter
* 📊 Visual progress meter
* 💰 Predicted house price
* 🔘 Interactive prediction button

This feature makes the machine learning prediction more interactive and user-friendly.

---

## 📁 Project Structure

```text
House-Price-Prediction/
│
├── finalproject(1).ipynb
├── train.csv
├── README.md
└── screenshots/
    └── dashboard.png
```

> If `train.csv` is not included in the repository, update the dataset path in the notebook before running it.

---

## ▶️ How to Run the Project

### 1. Clone the Repository

```bash
git clone <your-github-repository-url>
```

### 2. Navigate to the Project Folder

```bash
cd House-Price-Prediction
```

### 3. Install Required Libraries

```bash
pip install pandas numpy matplotlib seaborn plotly scikit-learn ipywidgets jupyter
```

### 4. Open Jupyter Notebook

```bash
jupyter notebook
```

### 5. Open the Notebook

Open:

```text
finalproject(1).ipynb
```

### 6. Update Dataset Path

The notebook currently contains a local Windows path for `train.csv`.

For example:

```python
df = pd.read_csv(r"C:\Users\nathu\Downloads\train.csv")
```

When running the project from GitHub, change this to the location of `train.csv` in your repository, for example:

```python
df = pd.read_csv("train.csv")
```

### 7. Run All Cells

Run the notebook cells from top to bottom to perform:

```text
Data Loading
      ↓
Data Exploration
      ↓
Missing Value Analysis
      ↓
Data Cleaning
      ↓
Preprocessing
      ↓
EDA & Visualization
      ↓
Model Training
      ↓
Model Evaluation
      ↓
Price Prediction
```

---

## 📈 Project Workflow

```text
Raw Housing Dataset
        │
        ▼
Data Understanding
        │
        ▼
Missing Value Analysis
        │
        ▼
Data Cleaning
        │
        ▼
Categorical Encoding
        │
        ▼
Train-Test / Validation Split
        │
        ▼
Feature Scaling
        │
        ▼
Machine Learning Models
   ┌────┴─────┐
   ▼          ▼
Linear     Random Forest
Regression  Regressor
   │          │
   └────┬─────┘
        ▼
Model Evaluation
        │
        ▼
House Price Prediction
        │
        ▼
⭐ PriceMeter
```

---

## 💡 Key Learnings

Through this project, the following concepts were implemented:

* Exploratory Data Analysis
* Data Cleaning
* Missing Value Handling
* Numerical & Categorical Feature Identification
* One-Hot Encoding
* Feature Scaling
* Train-Test Splitting
* Linear Regression
* Random Forest Regression
* Regression Model Evaluation
* Data Visualization
* Interactive Python Widgets
* House Price Prediction

---

## 👩‍💻 Team

### Group No. 16

* **Sakshi Sanjay Mohite**
* **Sanika Nathuram Ghadge**
* **Pallavi Sanjay Ghadge**
* **Nikita Prakash Todkar**

---

## 🚀 Future Improvements

Possible improvements for the project include:

* Hyperparameter tuning for the Random Forest model.
* Testing additional regression algorithms.
* Feature selection and engineering.
* Cross-validation.
* Improving the interactive prediction interface.
* Deploying the prediction model as a web application.
* Adding more detailed model comparison visualizations.

---

## 📜 License

This project is created for **educational and academic purposes**.

---

## ⭐ Acknowledgement

This project demonstrates the application of **Python, Exploratory Data Analysis, Data Visualization, and Machine Learning** for solving a real-world house price prediction problem.
