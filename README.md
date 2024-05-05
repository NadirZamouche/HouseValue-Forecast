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

## :chart_with_upwards_trend: Feature Importance
