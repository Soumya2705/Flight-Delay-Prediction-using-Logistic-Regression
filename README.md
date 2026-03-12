# ✈️ Flight Delay Prediction using Logistic Regression

## 📌 Project Overview

This project predicts whether a **flight will be delayed or not** using **Logistic Regression**, a supervised machine learning classification algorithm.

The dataset contains **historical airline flight data**, including airline information, airports, flight timings, and delay information.

The project demonstrates a complete **machine learning workflow**, including:

* Data preprocessing
* Handling class imbalance
* Model training
* Model evaluation

---

## 📂 Dataset

Since the dataset size is **greater than 500 MB**, GitHub does not allow direct upload.  
Therefore, the dataset is provided through a **Google Drive link**.

### 📊 Main Dataset

https://drive.google.com/file/d/1gkDTuB8LOStxfUf41VNvYWf_UfrHCzNL/view?usp=sharing

The dataset includes important flight attributes such as:

* Airline
* Origin Airport
* Destination Airport
* Departure Time
* Arrival Delay
* Distance
* Delay Causes

---

## 🛠️ Tools & Libraries Used

* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Seaborn
* Jupyter Notebook

---

## 🧹 Data Cleaning Steps

Before training the machine learning model, the dataset was cleaned and prepared.

Steps performed:

* Removed unnecessary columns
* Handled missing values
* Removed duplicate rows
* Encoded categorical variables
* Created the target variable **FLIGHT_DELAYED**
* Scaled numerical features using **StandardScaler**

These steps ensure the dataset is suitable for machine learning training.

---

## ⚖️ Handling Class Imbalance

The dataset contains **more non-delayed flights than delayed flights**, creating a class imbalance problem.

Two techniques were considered:

### Oversampling (SMOTE)

* SMOTE generates synthetic samples for the minority class.
* However, since the dataset contains **more than 1 million rows**, applying SMOTE significantly increases dataset size and training time.

Therefore **SMOTE was not used in this project.**

### Undersampling

Instead, **Random Undersampling** was applied.

Steps followed:

* Separated delayed and non-delayed flights
* Randomly sampled the majority class
* Created a balanced dataset with equal samples from both classes

This approach **reduces training time while improving model learning**.

---

## 📈 Model Implemented

### 1️⃣ Logistic Regression

A **Logistic Regression model** was used to classify flights into:

* **0 → Not Delayed**
* **1 → Delayed**

The model learns the relationship between flight features and the **probability of delay**.

---

## 🔍 Model Evaluation

The model performance was evaluated using:

* Accuracy
* Precision
* Recall
* F1 Score
* Confusion Matrix

### Model Performance

* **Accuracy:** ~84%
* **Precision:** ~0.86
* **Recall:** ~0.66
* **F1 Score:** ~0.74

These metrics help evaluate how well the model predicts delayed flights.

---

## 🚀 How to Run

1. Clone the repository
2. Download the dataset from the Google Drive link
3. Place the dataset in the project folder
4. Open **Flight_Delay_Prediction.ipynb**
5. Run the notebook step-by-step

---

## 🔮 Future Scope

Possible improvements include:

* Using advanced models such as **Random Forest or XGBoost**
* Performing **hyperparameter tuning**
* Adding **weather or time-based features**
* Building an **interactive dashboard**
* Deploying the model using **Flask or FastAPI**

---

## 📌 License

This project is created for **educational and learning purposes**.
