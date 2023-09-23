# Overview 

This repository houses documents for a project about forecasting the value of homes in Clark County, Nevada. The project’s purpose was to create an optimal ARIMA model for time series data in order to inform stakeholders on the types of zipcodes to target in this particular location. The main features of the repository are: 
* time_series folder:
  * <b>zillow.csv</b>: time series data that was filtered and used to build the ARIMA model. Because the dataset is large, it was placed inside of this folder so it could be uploaded to Github.
  * A Jupyter notebook with data preprocessing and time series analysis steps.
* A slides presentation for non-technical stakeholders 

# Business Context
This repository is applicable to real estate companies located in Clark County, Nevada, who are deciding on which zipcodes to invest in.  

The business question the project aimed to answer was: 
* <b>What are the Top 5 zipcodes in Clark County based on a projected 5-year ROI between 2018 and 2023?</b>  

# The Dataset
As touched upon previously, the dataset used for this project was <b>zillow.csv</b>. In the Jupyter notebook, this large dataset was reduced to a subset called <b>clark_df_filtered</b>, which only contained zipcodes located in Clark County, Nevada that had a <b>5-year ROI between 2013 and 2018 that was greater than or equal to 1.0 (100%)</b>. 

The image below shows a bar graph that represents the zipcodes featured in <b>clark_df_filtered</b>, along with their respective <b>5-year ROIs (2013-2018)</b>:

![image](https://github.com/jbenedito99/Zipcode-Time-Series-Modeling/assets/125815448/7701e0a9-9963-47aa-a39b-4680e0909063)

# ARIMA Modeling Results 
The final chosen ARIMA model for forecasting had an <b>order</b> of <b>(1, 1, 0)</b> and a <b>seasonal order</b> of <b>(1, 1, 0, 12)</b>. These optimal parameters were selected via a grid search method. In terms of performance, the model had an <b>RMSE</b> of <b>about 11,000</b>, which is higher than ideal. This metric indicates that the predictions for the mean value of houses in a zipcode were off by about $11,000.  

Pictured below is a graph of the ARIMA model's performance on one zipcode. We can see that the predicted values and true values stray farther away from each other as time goes on.

![image](https://github.com/jbenedito99/Zipcode-Time-Series-Modeling/assets/125815448/6fd648d1-da80-448f-89eb-10a2cb057918)

# Conclusions
Based on the forecasting performed by the final model, my suggestions are to invest in the following zipcodes:
* <b>89107</b>: 5-year ROI (2018-2023) of <b>about 125%</b>
* <b>89108</b>: 5-year ROI (2018-2023) of <b>about 112%</b>
* <b>89104</b>: 5-year ROI (2018-2023) of <b>about 111%</b>
* <b>89102</b>: 5-year ROI (2018-2023) of <b>about 109%</b>
* <b>89142</b>: 5-year ROI (2018-2023) of <b>about 95%</b>

![image](https://github.com/jbenedito99/Zipcode-Time-Series-Modeling/assets/125815448/3879c98a-8dc3-47b8-b7d9-f6cf4a9278e2)

# Sources and References
* [Presentation](https://docs.google.com/presentation/d/1JLzdTuIlCCfLuBinhpQ7khWfGZ7zDEcFditZRjjHTGg/edit?usp=sharing) 
* Some code used from [this source](https://github.com/sanjitva/Zillow-TimeSeries-Modeling/blob/main/final_notebook.ipynb)
* Function used from [this source](https://medium.com/@feraguilari/time-series-analysis-modfinalproyect-b9fb23c28309) 
