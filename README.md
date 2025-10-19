
# Predicting Customer Purchase Behavior Using Machine Learning

## Project Overview

This project analyzes customer behavior and predicts whether a customer will purchase a product using machine learning techniques. The dataset contains demographic and financial information for 400 clients, including age, estimated salary, and gender. The main goal is to understand the key factors influencing purchasing decisions and build a predictive model.

---

## Dataset

The dataset includes the following columns:

| Column          | Description                                               | Type   |
| --------------- | --------------------------------------------------------- | ------ |
| User ID         | Unique identifier for each customer                       | int64  |
| Gender          | Gender of the customer                                    | object |
| Age             | Age of the customer                                       | int64  |
| EstimatedSalary | Estimated annual salary of the customer                   | int64  |
| Purchased       | Whether the customer purchased the product (1) or not (0) | int64  |

* **Target variable:** `Purchased`
* **Features:** `User ID`, `Gender`, `Age`, `EstimatedSalary`

---

## Key Observations

### Univariate Analysis

* **Gender:** Almost equal distribution between males and females.
* **Purchased:** Fewer people decided to purchase a product than those who did not.
* **Age:** Ranges from 18 to 60 years.
* **EstimatedSalary:** Wide range from 15,000 to 150,000.

### Bivariate Analysis

* **Purchased vs Gender:** More females purchase a product than males, whereas more males do not purchase.
* **Purchased vs Age:** Strong positive correlation (0.62); older customers are more likely to purchase.
* **Purchased vs EstimatedSalary:** Customers who purchase have higher average salaries.
* **Gender vs EstimatedSalary:** Average salary is similar for males and females.

---

## Methodology

1. **Data Cleaning & Preprocessing**

   * Checked for missing and invalid values.
   * Standardized numerical features (Age and EstimatedSalary) due to differing scales.
   * Encoded categorical features where necessary (Gender).

2. **Model Selection**

   * **Multinomial Naive Bayes** was chosen because the dataset contains both discrete and continuous features.

3. **Model Evaluation**

   * Initial accuracy: 0.78
   * After improvements: 0.81
   * Confusion matrix and classification report indicate that class 1 (Purchased) has lower accuracy due to fewer examples.

---

## Code Structure

```
├── data/
│   └── customer_data.csv
├── notebooks/
│   └── customer_purchase_analysis.ipynb
├── README.md
└── requirements.txt
```

* `data/`: Contains the dataset.
* `notebooks/`: Jupyter Notebook with data analysis, visualization, and modeling steps.
* `requirements.txt`: Python dependencies.

---

## How to Run

1. Clone the repository:

2. Install dependencies:


3. Open the Jupyter Notebook in `notebooks/` and run all cells.

---

## Dependencies

* Python 3.x
* pandas
* numpy
* matplotlib
* seaborn
* scikit-learn

---

## Insights & Next Steps

* **Age and EstimatedSalary** are key predictors for purchasing behavior.
* **Gender** has minimal impact on prediction.
* To further improve the model:

  * Handle class imbalance using techniques like **SMOTE** or **class weighting**.
  * Try other classifiers like **Random Forest** or **XGBoost**.
  * Collect more data to improve predictions for the minority class.

