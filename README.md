# Taxi Pickup Density Forecasting Project

## Introduction

This project aims to forecast pickup densities for yellow taxi services in New York City. Accurate pickup density forecasting is crucial for taxi service companies to optimize their operations, enhance customer service, and increase revenue. To achieve this goal, we collect and analyze data provided by the NYC Taxi and Limousine Commission (TLC). This dataset encompasses various attributes such as pick-up and drop-off timestamps, locations, trip distances, fares, rate types, payment methods, and passenger counts. Our model leverages data from 2019-2020 for training and evaluates its performance using 2021 data.

## Dataset

The dataset used in this project can be accessed through the following link: [NYC TLC Trip Record Data](https://www1.nyc.gov/site/tlc/about/tlc-trip-record-data.page)

## Methodology

1. **Data Preparation**: We begin by cleaning and pre-processing the raw data. This involves handling missing values, encoding categorical features, and normalizing numerical attributes.

2. **Exploratory Data Analysis (EDA)**: Before constructing the forecasting model, we conduct exploratory data analysis to gain insights into the dataset's distribution, correlations, and trends. EDA guides our feature engineering and model selection.

3. **Model Selection**: For pickup density forecasting, we employ tree regressor algorithms. Two variations of the data are used for training:
   - **Ratio-based Approach (Rt)**: We feed the model ratios of 2021 data to 2019 data, i.e., Rt = Pt 2021 / Pt 2019.
   - **Value-based Approach**: The model is trained using 2019 data to predict values in 2021 and beyond.

4. **Evaluation Metrics**: We evaluate and compare the models using the Mean Absolute Percentage Error (MAPE) and Mean Squared Error (MSE) metrics. MAPE provides insights into prediction accuracy, while MSE measures the overall prediction error.

## Results and Future Work

Our analysis yields the following conclusions:

- Linear regression offers the best-performing model with its simplicity and relatively low MAPE values.
- In more complex scenarios, Xgboost emerges as the preferred technique for accurate taxi pickup density predictions.

Future avenues for improvement include:

1. **Incorporating Fourier Features**: Exploring the addition of Fourier features into regression models to assess their impact on MAPE.

2. **Hyperparameter Tuning**: Performing hyperparameter tuning for regression models to fine-tune their performance. This includes:
   - Linear Regression: Grid Search
   - Random Forest: Random Search
   - Xgboost: Random Search

3. **Time-Series Feature Exploration**: Continuously investigating additional time-series features to achieve a MAPE reduction target of less than 28%.

## About Hyperparameters

Machine learning models are defined by parameters that are learned from data during training. However, there are hyperparameters that dictate properties like model complexity and learning rate, which must be set before training. Hyperparameter optimization involves selecting optimal values to enhance model performance.

## Conclusion

Our project demonstrates the significance of accurate pickup density forecasting for taxi service companies. By leveraging data analysis and machine learning techniques, we provide insights into building effective models that aid in optimizing taxi operations and improving customer experiences. Our findings and recommendations pave the way for future research and enhancements in the field of taxi service optimization.
