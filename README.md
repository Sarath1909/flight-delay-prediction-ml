# flight-delay-prediction

✈️Predicting flight delays using Logistic Regression, Random Forest, and XGBoost with Kaggle dataset (2019–2023).

## 📌 Overview

This project predicts whether a flight will be delayed more than 5 minutes using machine learning models.
It uses the Kaggle [Flight Delay and Cancellation Dataset (2019–2023)](https://www.kaggle.com/datasets/patrickzel/flight-delay-and-cancellation-dataset-2019-2023?utm_source=chatgpt.com).

The goal is to showcase an end-to-end ML workflow:
- **Data preprocessing**
- **Feature engineering**
- **Model training (Logistic Regression, Random Forest, XGBoost)**
- **Model evaluation with precision, recall, F1, ROC-AUC**
---
## 📊 Dataset

Source: Kaggle (not included in this repo due to size/licensing)
Covers US flight delays & cancellations from 2019–2023
Features include: airline, origin, destination, scheduled departure/arrival, distance, etc.
Target variable:
    0 → On time (delay ≤ 5 min)
    1 → Delayed (delay > 5 min)

---
## ⚙️ Approach  

- **Data Preprocessing**  
  1. Missing value handling  
  2. Categorical encoding (OneHotEncoder)  
  3. Standard scaling for numerical features  

- **Models Trained**  
  1. Logistic Regression  
  2. Random Forest (with hyperparameter tuning)  
  3. XGBoost (with hyperparameter tuning)  

- **Evaluation Metrics**  
  1. Accuracy  
  2. Precision, Recall, F1-score  
  3. ROC-AUC  
  4. Confusion Matrix  

---
## 📈 Results (Summary)

| Model               | Accuracy | ROC-AUC | Notes                                |
|---------------------|----------|---------|--------------------------------------|
| Logistic Regression | ~0.58    | ~0.61   | Baseline model                       |
| Random Forest       | ~0.59    | ~0.60   | Better recall, balanced              |
| XGBoost             | ~0.68    | ~0.63   | Higher accuracy, but weaker recall   |

⚠️ Models struggle due to class imbalance (many flights are on-time). Improvements could come from SMOTE, class weights, or threshold tuning.

---
## 🚀 How to Run

Clone the repo:
git clone https://github.com/Sarath1909/flight-delay-prediction-ml.git
cd flight-delay-prediction-ml

Install dependencies:
pip install -r requirements.txt

Run the notebook:
jupyter notebook notebooks/flight_delay.ipynb

---
## 🔮 Next Steps

- **Handle class imbalance with SMOTE or re-weighting**
- **Try additional models (LightGBM, CatBoost, Neural Networks)**
- **Feature engineering (e.g., day of week, month, weather integration)**
- **Deploy as a simple API or web app for demonstration**

---
## 📂 Project Structure

flight-delay-prediction-ml/
│
├── notebooks/
│   └── flight_delay.ipynb     # main notebook
│
├── requirements.txt           # dependencies
├── README.md                  # project documentation
└── LICENSE

---
## 📜 License

This project is released under the MIT License.

---
🙋‍♂️ Author

Sarath Santhosh
GitHub: [Sarath Santhosh](https://github.com/Sarath1909)
LinkedIn: [Sarath Santhosh](https://www.linkedin.com/in/sarathsanthosh1909)
