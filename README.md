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
* Used OneHotEncoder on the 3 which is a categorical columns.
* Filled missing values using mean strategy.
* Created boxplots for each column to check for outliers. Here is a box plot for Monthly Income column:
  <img width="584" alt="Box Plot for Population" src="https://github.com/NadirZamouche/HouseValue-Forecast/assets/95188070/73fcc612-fbb7-4f4c-8c9b-86496dbbb4f3">


* Ploted histograms for each column to see if the data is balanced or not:

  <img width="736" alt="Histograms" src="https://github.com/FlammeTik/AI_HR_Attrition/assets/95188070/4149b177-dd7c-4291-b23c-7d48accd7d83">

* Ploted heat map for correlation matrix:

  <img width="671" alt="Correlation Matrix" src="https://github.com/FlammeTik/AI_HR_Attrition/assets/95188070/82b16f3b-4271-4d30-bebf-f8c476194267">

* Applied the standard scaler since there were outliers within the data.
* Created the data pipeline encompassing all transformation steps for later use in machine learning.

## :desktop_computer:	Modeling

## :chart_with_upwards_trend: Feature Importance
