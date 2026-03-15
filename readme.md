# Customer Churn Prediction Using Artificial Neural Networks (ANN)

## 📖 Project Overview

Customer churn occurs when customers or subscribers stop doing business with a company or service. Retaining existing customers is often much more cost-effective than acquiring new ones. 

This project is an **end-to-end Machine Learning pipeline** that predicts the likelihood of a bank customer churning. It uses an **Artificial Neural Network (ANN)** built with TensorFlow and Keras to classify customers into "likely to churn" or "not likely to churn" based on their demographic and financial activity data. 

The project goes beyond just model training by including hyperparameter tuning, regression analysis (for salary prediction), and a **Streamlit web application** that allows users to input customer data and get real-time churn predictions.

---

## 📊 Dataset Features (Data Dictionary)

The model is trained on a dataset containing the following customer attributes. These are the exact features you can adjust in the Streamlit app to test different prediction scenarios:

| Feature | Type | Description |
| :--- | :--- | :--- |
| **Geography** | Categorical | The country where the customer resides (France, Germany, or Spain). |
| **Gender** | Categorical | The customer's gender (Male or Female). |
| **Age** | Numerical | The customer's age (between 18 and 92 years). |
| **Credit Score** | Numerical | A score representing the customer's creditworthiness. |
| **Balance** | Numerical | The amount of money the customer has in their bank account. |
| **Estimated Salary** | Numerical | The customer's estimated annual salary. |
| **Tenure** | Numerical | The number of years the customer has been with the bank (0 to 10). |
| **Number of Products** | Numerical | The number of bank products the customer uses (e.g., savings account, credit card, etc. Range: 1 to 4). |
| **Has Credit Card** | Binary | Whether the customer has a credit card with the bank (1 = Yes, 0 = No). |
| **Is Active Member** | Binary | Whether the customer is an active member with the bank (1 = Yes, 0 = No). |
| **Target Variable (Churn)** | Binary | The prediction output: `1` (Likely to Churn) or `0` (Not Likely to Churn). |

*Note: Categorical features are converted using One-Hot Encoding and Label Encoding, while numerical features are scaled using Standard Scaling before being passed into the neural network.*

---

## 📂 Project Structure

* **`app.py`**: The main Streamlit web application. It loads the trained ANN model and pre-processing objects to provide an interactive UI for real-time customer churn prediction.
* **`expe.ipynb`**: A Jupyter Notebook containing initial data exploration, data preprocessing, model training, and TensorBoard integration for visualizing training performance.

* **`predict.ipynb`**: A concise script demonstrating how to load the saved model and encoders to make a single churn probability prediction on new data.

* **`requirements.txt`**: A list of all Python dependencies required to run the notebooks and the Streamlit app.

### Preprocessing & Model Artifacts
These exported files are used by the Streamlit app to ensure incoming data is formatted exactly like the training data:
* `model.h5`: The compiled and trained Keras ANN model.
* `scaler1.pkl`: The StandardScaler object used to normalize numerical inputs.
* `label_encoder_gender1.pkl`: The LabelEncoder for the 'Gender' feature.
* `onehot_encoder_geo1.pkl`: The OneHotEncoder for the 'Geography' feature.

---

## 🛠️ Technology Stack

* **Deep Learning Framework:** TensorFlow & Keras
* **Machine Learning Tools:** Scikit-Learn (for Scaling, Encoding)
* **Data Manipulation:** Pandas, NumPy
* **Web Framework:** Streamlit
* **Visualization:** TensorBoard, Matplotlib

---

## 🚀 Getting Started

### Prerequisites

Ensure you have Python installed (preferably Python 3.9 - 3.11 for compatibility with TensorFlow 2.15.0).

### Installation

1. Clone or download this repository.
2. Navigate to the project directory in your terminal.
3. Install the required dependencies:

```bash
pip install -r requirements.txt
```