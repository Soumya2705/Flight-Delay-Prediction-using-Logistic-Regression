✈️ Flight Delay Prediction using Logistic Regression
📌 Project Overview

This project predicts whether a flight will be delayed or not delayed using Logistic Regression, a supervised machine learning classification algorithm.

The dataset contains historical airline flight data, including airline information, origin and destination airports, flight schedules, and delay details.

The project demonstrates a complete machine learning workflow, including data preprocessing, handling class imbalance, model training, and model evaluation.

📂 Dataset

Since the dataset size is greater than 500 MB, GitHub does not allow direct upload.
Therefore, the dataset is provided through a Google Drive link.

📊 Main Dataset

https://drive.google.com/file/d/1gkDTuB8LOStxfUf41VNvYWf_UfrHCzNL/view?usp=sharing

🛠️ Tools & Libraries Used

Python

Pandas

NumPy

Scikit-learn

Matplotlib

Seaborn

Jupyter Notebook

🧹 Data Cleaning Steps

Several preprocessing steps were performed before training the model:

Removed unnecessary columns

Handled missing values

Removed duplicate records

Converted categorical columns using encoding

Created the target variable FLIGHT_DELAYED

Scaled numerical features using StandardScaler

These steps helped prepare the dataset for machine learning.

⚖️ Handling Class Imbalance

The dataset contains more non-delayed flights than delayed flights, which creates a class imbalance problem.

Two techniques were considered to address this issue:

SMOTE (Oversampling)

SMOTE generates synthetic samples for the minority class.

However, since the dataset contains more than 1 million rows, applying SMOTE significantly increases the dataset size and training time.
Therefore, SMOTE was not used in this project due to its high computational cost.

Undersampling

Instead, random undersampling was applied to balance the dataset.

Steps followed:

Separated delayed and non-delayed flights

Randomly sampled the majority class

Created a balanced dataset with equal samples from both classes

This approach improves model learning while keeping training time manageable.

📈 Model Implemented
1️⃣ Logistic Regression

A Logistic Regression model was used to classify flights into:

0 → Not Delayed
1 → Delayed

The model learns the relationship between flight features and the probability of a delay.

🔍 Model Evaluation

The model performance was evaluated using several classification metrics:

Accuracy

Precision

Recall

F1 Score

Confusion Matrix

Model Performance
Accuracy  : ~84%
Precision : ~0.86
Recall    : ~0.66
F1 Score  : ~0.74

These metrics provide insights into how well the model predicts flight delays.

📊 Confusion Matrix Interpretation

The confusion matrix helps understand the prediction results:

True Positive (TP) → Correctly predicted delayed flights

True Negative (TN) → Correctly predicted non-delayed flights

False Positive (FP) → Predicted delay but flight was not delayed

False Negative (FN) → Delayed flight predicted as not delayed

This helps analyze where the model performs well and where improvements are needed.

🚀 How to Run

Clone the repository

Download the dataset from the Google Drive link

Place the dataset in the project folder

Open flight_delay_prediction.ipynb

Run the notebook step-by-step

🔮 Future Scope

Possible improvements for this project include:

Applying advanced machine learning models such as Random Forest or XGBoost

Performing hyperparameter tuning

Creating additional time-based or route-based features

Building an interactive flight delay prediction dashboard

Deploying the model as a web application

📌 License

This project is created for educational and learning purposes
