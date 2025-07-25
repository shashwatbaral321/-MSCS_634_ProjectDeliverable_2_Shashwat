# 📊 Linear Regression Lab Report

**Course**: Advanced Big Data and Data Mining (MSCS-634-B01) 
**Student**: Shashwat Baral
**Lab Topic**: Linear Regression Analysis on Country Data  

---

## 🧪 Purpose of the Lab

The objective of this lab was to develop a linear regression model utilizing a real-world dataset that encompasses country-level data, aiming to predict a numerical value (indicative of GDP or an economic index) through encoded features such as country name, region, and year. The lab sought to furnish practical experience in data preprocessing, model training, evaluation, and result interpretation using Python and scikit-learn.

---

## 📁 Dataset Summary

The dataset comprised 225 entries, each corresponding to a country in a specific year, featuring attributes such as:

- `name`: Country name  
- `slug`: A slug identifier (excluded)  
- `region`: Geographical region  
- `value`: The target variable (e.g., GDP) formatted as a string with commas  
- `date_of_information`: Year of data  
- `ranking`: Relative position among other countries

Following preprocessing, the dataset was modified to incorporate 670 numerical features through one-hot encoding.

---

## 🔧 Modeling Process

1. **Data Cleaning**: Eliminated unnecessary columns and converted `value` to float.
2. **Encoding**: Implemented one-hot encoding for categorical columns.
3. **Feature Scaling**: Employed `StandardScaler` to normalize features.
4. **Train-Test Split**: 80/20 train-test ratio.
5. **Modeling**: Utilized `LinearRegression` from Scikit-learn.
6. **Evaluation**: Evaluated the model using various performance metrics.

---

## 📈 Evaluation Results

- **R² Score**: `0.9996` – indicative of excellent explanatory power  
- **Mean Absolute Error (MAE)**: `636.22`  
- **Mean Squared Error (MSE)**: `1,342,870.37`  
- **Root Mean Squared Error (RMSE)**: `1,158.82`  

These findings suggest that the model was exceptionally proficient at discerning patterns within the training data and exhibited strong performance on the test set.

---

## 💡 Key Insights

- The implementation of one-hot encoding significantly expanded the feature space, yet it proved effective in this instance.
- The model successfully accounted for over 99% of the variance in the target variable.
- Even with substantial values in the target variable, the prediction errors remained minimal.

---

## ⚠️ Challenges and Decisions

- **Data Cleaning**: The `value` column necessitated transformation due to formatting problems (commas, string type).
- **Byte Order Mark**: The `name` column contained a BOM (`ï»¿name`), which was addressed through the use of `utf-8-sig` encoding.
- **Overfitting Concerns**: The use of one-hot encoding resulted in the creation of hundreds of features, which could potentially lead to overfitting. Although the performance was robust, future models might benefit from implementing feature selection or regularization techniques.

---

## ✅ Conclusion

The laboratory exercise illustrated the entire linear regression process, from data cleaning to evaluation. The model achieved nearly flawless performance on the test dataset. In subsequent applications, techniques for dimensionality reduction or regularized regression methods such as Ridge or Lasso may prove advantageous.
