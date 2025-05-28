# Practical Lab 1 – Linear Regression Analysis on California Housing Dataset

## Overview

This lab explores simple linear regression using selected features from the California Housing dataset. The goal is to evaluate the predictive performance of individual features on median housing prices and compare their effectiveness based on standard regression metrics.

## Dataset

The dataset used is the **California Housing Prices** dataset, which can be accessed through:


- downloadable from Kaggle:
```bash
  curl -L -o ~/Downloads/california-housing-prices.zip \
  https://www.kaggle.com/api/v1/datasets/download/camnugent/california-housing-prices
```
## Objectives

1. **Load and inspect** the California housing dataset.  
2. **Select and visualize** individual features.  
3. **Apply simple linear regression** for each selected feature.  
4. **Evaluate the model** using:  
   - Mean Squared Error (MSE)  
   - Mean Absolute Error (MAE)  
5. **Interpret and summarize** findings. 

## Selected Features

The following three features were used to predict the median house value:

- `median_income`
- `population`
- `households`

## Model Evaluation Results

| Feature        | Intercept       | Slope          | MSE            | MAE            |
|----------------|------------------|----------------|----------------|----------------|
| median_income | 45085.576703     | 41793.849202   | 7.01e+09       | 62625.933791   |
| population     | 210436.262076    | -2.511753      | 1.33e+10       | 91153.820095   |
| households     | 196928.577162    | 19.872775      | 1.33e+10       | 90802.743243   |

## Conclusion

Among the three models evaluated, the linear regression model using `median_income` as the independent variable provided the best fit. It achieved the lowest Mean Squared Error (MSE) and Mean Absolute Error (MAE), indicating a stronger predictive relationship with median house value compared to `population` and `households`.

Key insights:

- **Median Income** shows a strong positive correlation with house value. This is expected, as income levels typically influence real estate prices.
- **Population** and **Households**, while relevant, exhibited higher error rates and less explanatory power when modeled independently.
- Feature selection has a significant impact on model performance. In future work, combining multiple features or using advanced regression techniques (e.g., multiple linear regression or regularization) could yield better results.

## Output

To generate the HTML output from the Jupyter notebook, the following command was used:

```bash
jupyter nbconvert --to html "Practical_Lab_1.ipynb" --output-dir "outputs"

```

## How to Run

1. Clone the repository or download the `Practical_Lab_1.ipynb` notebook.
2. Install required libraries using pip if not already installed:

 ```bash
   pip install pandas numpy matplotlib scikit-learn jupyter
```
