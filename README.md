# 🚢 Titanic Survival Prediction - Logistic Regression

This project uses logistic regression to predict whether a passenger survived the Titanic disaster, based on features like class, fare, gender, and embarkation point. It is a classic binary classification problem from the Seaborn Library and [Kaggle Titanic dataset](https://www.kaggle.com/c/titanic).

---

## 📂 Dataset

- Dataset: Titanic - Machine Learning from Disaster
- Source: [Kaggle Titanic Dataset](https://www.kaggle.com/c/titanic)
- Features used:
  - `pclass`: Ticket class
  - `fare`: Passenger fare
  - `sex`, `who`, `adult_male`: Passenger gender and type
  - `embark_town`: Port of embarkation
  - `alone`: Whether the passenger was alone

---

## 🧪 Exploratory Data Analysis (EDA)

- Checked for null values
- Explored distributions of numerical features
- Visualized correlations using heatmaps
- Analyzed survival distribution by gender, class, and embarkation town

---

## 🛠️ Data Preprocessing

- Filled missing values
- Converted categorical columns to numeric using `pd.get_dummies()` with `drop_first=True`
- Removed duplicate or irrelevant columns
- Scaled numerical features using `StandardScaler`
- Split dataset into training and testing sets using `train_test_split`

---

## 🤖 Model Building

- Model used: `LogisticRegression` from `sklearn`
- Training on 75% of data, testing on 25%
- Fit the model using:
  
  ```python
  log_model.fit(X_train, y_train)
  ```

---

## 📊 Model Evaluation

- Evaluated using classification report and accuracy score

```
Accuracy: 77%
Precision: Good balance between classes
Recall: Higher for class 0 (did not survive)
F1-Score: Balanced around 0.72 to 0.80
```

- You can also evaluate using:

```python
from sklearn.metrics import classification_report
print(classification_report(y_test, y_pred))
```

---

## 📈 Future Improvements

- Try more models: Random Forest, XGBoost, or SVM
- Handle class imbalance (e.g. SMOTE, weighted loss)
- Include more features like age, cabin, or family size
- Perform hyperparameter tuning (GridSearchCV)

---

## 🚀 How to Run

1. Clone this repo:
   ```bash
   git clone https://github.com/Evertte/titanic-logistic-regression.git
   cd titanic-logistic-regression
   ```

2. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn
   ```

3. Run the notebook or script:
   ```bash
   jupyter notebook Titanic_Logistic_Regression.ipynb
   ```

---


- 🎓 Project done as part of learning logistic regression and model evaluation.

---

## 📜 License

This project is open source and available under the [MIT License](LICENSE).
