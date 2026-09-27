# 🚀 Spaceship Titanic - Kaggle Competition

Machine Learning solution for the **Spaceship Titanic** Kaggle competition.

## 📌 Competition

The goal is to predict whether a passenger was **Transported** to another dimension based on passenger information, cabin details, and spending behavior.

**Task:** Binary Classification  
**Metric:** Accuracy

---

## 📊 Dataset

The dataset contains passenger information such as:

- PassengerId
- HomePlanet
- CryoSleep
- Cabin
- Destination
- Age
- VIP
- RoomService
- FoodCourt
- ShoppingMall
- Spa
- VRDeck
- Transported

---

## 🛠️ Feature Engineering

I created additional features from the original dataset.

### Cabin Features

The `Cabin` column was split into:

- `cd` → Cabin Deck
- `cn` → Cabin Number
- `cs` → Cabin Side

### PassengerId Features

`PassengerId` was split into:

- `grpid` → Group ID
- `person_number` → Passenger number within the group
- `grp_size` → Number of passengers in the group

### Spending Features

Created:

- `TotalSpend` → Total amount spent across services
- `ServicesUsed` → Number of services used

---

## 🤖 Models Tested

The following models were evaluated:

### Logistic Regression
Validation Accuracy: ~79%

### XGBoost
Validation Accuracy: **81.94%**

### CatBoost
Validation Accuracy: **81.37%**

XGBoost achieved the highest validation accuracy among the tested models.

---

## 🏆 Final Model

The final submission was generated using:

**XGBoost Classifier**

The model was trained using:

- One-Hot Encoding for categorical features
- Numerical features
- Engineered cabin features
- Passenger group features
- Spending features

---

## 📈 Validation Result

| Model | Accuracy |
|---|---:|
| Logistic Regression | ~79% |
| CatBoost | 81.37% |
| XGBoost | **81.94%** |

---

## 📁 Project Structure

```text
Spaceship-Titanic/
│
├── train.csv
├── test.csv
├── sample_submission.csv
├── submission_xgboost.csv
├── notebook.ipynb
└── README.md
