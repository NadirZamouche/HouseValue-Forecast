## 📝 Description
This project aims to predict housing prices based on various factors using machine learning techniques. It utilizes five regression models, with Gradient Boosters demonstrating the lowest margin of errors. Additionally, hyper-parameter tuning was performed to further enhance model performance.

## ⏳ Dataset
The 'housing.csv'  file contains data on various attributes. Here's a breakdown of each column:
- Longitude: The longitude coordinates of the housing location.
- Latitude: The latitude coordinates of the housing location.
- Housing_median_age: The median age of houses in the area.
- Total_rooms: Total number of rooms in the housing unit.
- Total_bedrooms: Total number of bedrooms in the housing unit.
- Population: Total population of the area.
- Households: Total number of households in the area.
- Median_income: Median income of households in the area.
- Median_house_value: Median value of houses in the area.
- Ocean_proximity: Proximity of the housing area to the ocean (e.g., 'Near Bay', 'Inland', 'Near Ocean', etc.).

## :mag: Data Cleansing
* Filled missing values using mean strategy.
* Used OneHotEncoder on ocean_proximity (categorical column).
* Created boxplots for each column to check for outliers. Here is a box plot for Population column:
  
  <img width="584" alt="Box Plot for Population" src="https://github.com/NadirZamouche/HouseValue-Forecast/assets/95188070/73fcc612-fbb7-4f4c-8c9b-86496dbbb4f3">


* Ploted histograms for each column to see if the data is balanced or not:

  <img width="479" alt="Histograms" src="https://github.com/NadirZamouche/HouseValue-Forecast/assets/95188070/6ecbee0a-c8c3-4504-ace5-3ea7e99e78ed">


* Ploted heat map for correlation matrix:

  <img width="460" alt="Correlation Matrix" src="https://github.com/NadirZamouche/HouseValue-Forecast/assets/95188070/806171c4-c0fe-44c0-b84b-f5a7af737dd1">


* Applied the standard scaler since there were outliers within the data.
* Created the data pipeline encompassing all transformation steps for later use for modeling.

## :desktop_computer:	Modeling
* Utilizing the previous data pipeline. I partitioned the data into two sets: 75% designated for training and 25% allocated for testing. Also, since we're in a situation of regression I couldn't use the StratifiedShuffleSplit as I used to in classfication splits.
* Employed five distinct regression models, systematically assessing for overfitting through cross-validation techniques. Subsequently, I computed various evaluation metrics for each model and discerned the optimal choice based on MAE (Mean Absolute Error).

<img width="473" alt="Evaluation Metrics" src="https://github.com/NadirZamouche/HouseValue-Forecast/assets/95188070/b0a51247-230a-4854-b6dd-ad67f3d6fdd6">

* Conducted hyper-parameter tuning for eXtream Gradient Bossting Regressor, meticulously exploring various settings to ascertain the most effective combination for optimal performance.

<img width="262" alt="Best Parameters Combination" src="https://github.com/NadirZamouche/HouseValue-Forecast/assets/95188070/bb93ef3d-9468-4a54-b284-2368f58f5512">

* Tested the final model on the test set and got relatively better results:

<img width="162" alt="Evaluation Metrics (Tuned Model)" src="https://github.com/NadirZamouche/HouseValue-Forecast/assets/95188070/479970f1-28d1-4e94-8443-9d838507afc5">

* Retested the final model on the whole entry dataset and got even better results:

<img width="134" alt="Evaluation Metrics (Whole Set)" src="https://github.com/NadirZamouche/HouseValue-Forecast/assets/95188070/f96d4cf8-9219-4af4-8b81-2fe07b42dc13">

## :chart_with_upwards_trend: Feature Importance
* Here is a chart showing the sorted contribution of each column to the target column "median_house_value":

<img width="459" alt="Feature Importance" src="https://github.com/NadirZamouche/HouseValue-Forecast/assets/95188070/588f84d1-4657-499e-8f8a-64ea290257ef">

## 🔨 Conclusion
The analysis highlights the importance of ocean proximity, particularly being inland, followed by island properties, in predicting house prices. Additionally, median income is also a significant factor in determining housing prices, although slightly less influential compared to ocean proximity. This information can be valuable for understanding the drivers of housing market dynamics and making informed decisions in real estate investments or policy-making.
This model has shown very excellent results since the marginal error is very small, therfore it can be implemented for later use as you can see in this illustration:

<img width="258" alt="Results" src="https://github.com/NadirZamouche/HouseValue-Forecast/assets/95188070/4ca5fba8-4bcb-4370-9d8b-4b050bb8197b">

