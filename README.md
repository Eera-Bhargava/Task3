# Task3
# Housing Price Prediction using Linear Regression

This project performs data preprocessing, model training, and evaluation using a **Linear Regression** model on a Housing dataset.


## Objectives
1. Import and preprocess the dataset.
2.Split data into train-test sets.
3.Fit a Linear Regression model using  `sklearn.linear_model`.
4.Evaluate model using MAE, MSE, R².
5.Plot regression line and interpret coefficients.

## Dataset

The dataset `Housing.csv` includes the following columns:

- **Numerical features:** `area`, `bedrooms`, `bathrooms`, `stories`, `parking`, etc.  
- **Categorical features:** `mainroad`, `guestroom`, `basement`, `hotwaterheating`, `airconditioning`, `furnishingstatus`, `prefarea`  
- **Target variable:** `price`


### Data Preprocessing
- Categorical columns like `mainroad`, `guestroom`, etc., are label encoded as binary (`yes` → 1, `no` → 0).
- `furnishingstatus` is one-hot encoded using `pd.get_dummies()`, dropping the first category to avoid dummy variable trap.

### Splitting the Data
- The data is split into features `X` and target `y = price`.
- Used `train_test_split` from `sklearn` to create training and testing sets.

### Model Training
- A Linear Regression model is created using:
```python
from sklearn.linear_model import LinearRegression
