# Time Series Sales Forecasting for Walmart Sales 

## Abstract

This project focuses on evaluating various time series forecasting methods to predict sales for a given item. The dataset used is derived from Walmart sales data. We explore and compare different techniques, including a naive approach, Simple Moving Averages, Exponential smoothing, SARIMAX, and Facebook's Prophet model. The evaluation metric employed is the Root Mean Square Error (RMSE). Our findings indicate that models utilizing a moving average window size of 2 and SARIMAX exhibit the best performance. Future enhancements could involve extensive hyperparameter tuning and integration of additional datasets such as weather and natural disaster data.

## Introduction

In this study, we employ five fundamental statistical models for time series forecasting, selecting the optimal model based on its performance with our sales dataset. The following section provides an overview of the models used in our analysis:

1. **Naive Approach**: This approach forecasts sales by simply predicting tomorrow's sales value as today's sales value.

2. **Simple Moving Averages**: Averages of the previous n days' sales values are used to predict today's sales value, where n is the window size.

3. **Exponentially Weighted Moving Averages**: A weighted average of previous time steps, incorporating both actual and predicted values, is employed for forecasting.

4. **SARIMAX**: A Seasonal Auto-Regressive Integrated Moving Average model with eXogenous factors is used, incorporating auto-regressive, moving average, and seasonal components.

5. **Facebook's Prophet Model**: Prophet employs additive modeling with trend, yearly seasonality, weekly seasonality, and user-defined holidays.

## Data

Link to the dataset: https://www.kaggle.com/competitions/m5-forecasting-accuracy

### About the dataset

The dataset consists of dimensions 30490 x 1947, signifying data for 30,490 distinct items. Each row corresponds to a unique item, store, and state combination. The dataset encompasses a time span of 1941 days, representing sales data.

The structure of the dataset includes 6 columns denoting attributes specific to each item. The remaining columns pertain to the item's daily sales records over the 1941-day period. The non-day columns are outlined as follows:
<img width="420" alt="image" src="https://github.com/Bri1201/Sales-Forecast/assets/95512985/7e4ace31-6fc5-4eb6-9084-4b7501085a84">

Some attributes of our dataset are as follows:
● 3 states: ['CA', 'TX', 'WI'].
● 10 stores: ['CA_1', 'CA_2', 'CA_3', 'CA_4', 'TX_1', 'TX_2', 'TX_3', 'WI_1', 'WI_2',
'WI_3'].
● 3 categories: ['HOBBIES' 'HOUSEHOLD' 'FOODS'].
● 7 departments: ['HOBBIES_1', 'HOBBIES_2', 'HOUSEHOLD_1', 'HOUSEHOLD_2',
'FOODS_1', 'FOODS_2', 'FOODS_3'].
● 3049 items.
● Total Number of Time Series: 30490.
This can be visualized as follows:

<img width="381" alt="image" src="https://github.com/Bri1201/Sales-Forecast/assets/95512985/200a8269-22e1-4250-a04c-a90f65d5cb32">


## Model Explanations

1. **Naive Approach**: Ŷt+1 = Yt

2. **Simple Moving Averages**: Ŷt+1 = 1/n * ∑(j=t-n)Yj

3. **Exponentially Weighted Moving Averages**: Ŷt+1 = α*Yt + (1-α)*Ŷt

4. **SARIMAX**: Ŷt+1 = ø + θtYt + θt-1Yt-1 + ... + θt-pYt-p + ε

5. **Facebook's Prophet Model**: Additive regression model with trend, yearly and weekly seasonality, and user-provided holidays.

## Results and Future Work

Our analysis reveals that the moving average model with a window size of 2 and SARIMAX demonstrate the best performance in sales forecasting based on RMSE. Future work could involve:

- Extensive Hyperparameter Tuning: Further optimizing hyperparameters of SARIMAX and Prophet models for improved accuracy.
- Incorporation of Additional Datasets: Integration of external data sources such as weather and natural disaster data to enhance prediction capabilities.

## Error Metrics

We evaluate our models using the Root Mean Square Error (RMSE), which measures the accuracy of predictions relative to actual values. Percentage errors like mean absolute percentage error and symmetric mean absolute percentage error are not used due to the presence of zero values in our data.

## Final Prediction

After extensive evaluation of various time series forecasting methods, we have determined that simple moving averages, with a window size of 2, provide the most accurate predictions. To arrive at our final prediction, we applied the simple moving averages approach to all models and calculated the RMSE value.

Our final RMSE value for the entire dataset is: **6.467554362337222**

## VII. Conclusion and Future Work

From our comprehensive analysis, it is evident that two smoothing methods, namely moving average and SARIMAX, emerge as the top-performing models. On the other hand, the naive approach and Prophet model exhibit inferior performance. However, we strongly believe that the accuracy of the SARIMAX and Prophet models can be substantially enhanced through hyperparameter tuning.

In the future, further improvements in sales forecasting can be achieved by introducing additional features to the dataset, such as holidays and weather data. Additionally, within the realm of time series analysis, employing more advanced techniques for hyperparameter tuning has the potential to significantly elevate the accuracy and effectiveness of the models.

This project serves as a foundation for more accurate and insightful sales predictions, and it provides valuable insights for ongoing research and exploration in the field of time series forecasting. By continuously refining our methods and incorporating more comprehensive data, we can unlock even greater potential for accurate sales predictions and strategic decision-making.

<img width="615" alt="image" src="https://github.com/Bri1201/Sales-Forecast/assets/95512985/d0c9c6f0-cfe0-4459-9b1f-c625927cce35">


