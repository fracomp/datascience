PORTFOLIO 1:

DATA: cheetah.csv and strava_export.csv

OBJECTIVE: The first portfolio is based on a set of data on Steve's cycling history over the last couple of years exported from a couple of different systems. This is an exercise in data manipulation and data exploration using Pandas Data Frames.

DATA DESCRIPTION:
Here are definitions of some of the more important fields in the data. Capitalised fields come from the GoldenCheetah data
while lowercase_fields come from Strava.
  * distance - distance travelled in Km
  * moving_time: spent moving (not resting or waiting at lights)
  * Elevation Gain: metres climbed over the ride
  * Average Speed: average speed over the ride in km/h
  * average_watts: average power in watts as measured by a power meter, relates to how much effort is being put in to the ride
  * average_heartrate - average heartrate per ride
  * NP - Normalised Power, a smoothed average power measurement, generally higher than Average Power 
  * TSS - Training Stress Score, a measure of how hard a ride this was
  * kudos - likes from other Strava users (social network)
  * workout_type - one of  'Race',  'Workout' or  'Ride'
  
CONCLUSION:
Some of the most interesting findings in the dataset were:
  * The combined dataset (cheetah.csv and strava_export.csv) contains 243 rows and 372 columns
  * After removing the outliers, the distribution of 'Average_speed' looks normally distributed and this is also conformed by the     normality test
  * Distance and TSS are strongly related as well as Elevation gain with Distance and moving time with TSS
  * The median speed of the cyclist is much higher when there is a race involved.
  * The 'Ride' sessions are those where the cyclist does not use much power and therefore the average heartrate remains small. On     the other hand, the 'Race' rides are those that demands much more power and this leads an increase of the heartrate.
  * Workout type and distance seem to be the main factors to consider in order to get more kudos.
  * November 2019 was the month where the cyclist rode the most with almost 700 kilometers travelled.






PORTFOLIO 2:

DATA: 'energydata_complete.csv' -> Complete dataset
      'training.csv' -> Training data
      'testing.csv' -> Testing data

OBJECTIVE: The goal of the second portfolio is to reproduce some work on predicting the energy usage of a house based on IoT measurements of temperature and humidity and weather observations.  
An exploration of the data showing the distribution of values of variables that matches some of the plots shown in the first part of the paper is also required. 
The last goal is fitting a linear model to the data and generating evaluation metrics (root mean squared error, R2) 
Use the sklearn RFE function to apply Recursive Feature Estimation to the data to select the best features, compare with the results described in the paper for the same operation.


DATA DESCRIPTION:
date time year-month-day hour:minute:second 
  * Appliances, energy use in Wh
  * lights, energy use of light fixtures in the house in Wh
  * T1, Temperature in kitchen area, in Celsius
  * RH_1, Humidity in kitchen area, in %
  * T2, Temperature in living room area, in Celsius
  * RH_2, Humidity in living room area, in %
  * T3, Temperature in laundry room area
  * RH_3, Humidity in laundry room area, in %
  * T4, Temperature in office room, in Celsius
  * RH_4, Humidity in office room, in %
  * T5, Temperature in bathroom, in Celsius
  * RH_5, Humidity in bathroom, in %
  * T6, Temperature outside the building (north side), in Celsius
  * RH_6, Humidity outside the building (north side), in %
  * T7, Temperature in ironing room , in Celsius
  * RH_7, Humidity in ironing room, in %
  * T8, Temperature in teenager room 2, in Celsius
  * RH_8, Humidity in teenager room 2, in %
  * T9, Temperature in parents room, in Celsius
  * RH_9, Humidity in parents room, in %
  * To, Temperature outside (from Chièvres weather station), in Celsius
  * Pressure (from Chièvres weather station), in mm Hg
  * RH_out, Humidity outside (from Chièvres weather station), in %
  * Windspeed (from Chièvres weather station), in m/s
  * Visibility (from Chièvres weather station), in km
  * Tdewpoint (from Chièvres weather station), °C
  * rv1, Random variable 1, nondimensional
  * rv2, Rnadom variable 2, nondimensional

CONCLUSION:
Some of the most interesting findings in the dataset were:

  * The energy consumption profile shows a high variability with periods of almost constant demand followed by high spikes.
  * The energy consumption distribution is not symmetric and therefore skewed to the right. The majority of the values are within     the range 0 to 180 Wh.
  * The highly correlated features with the output variable are 'lights','RH_out' and 'NSM'. 
  * The model is only able to explain 8% of the total variance in the energy consumption of appliances when the filter method is     applied for feature selection.
  * The optimal number of features is 24 (24/30) when RFE is applied. A linear regression with the most important 24 predictors       produces almost 15% accuracy.
  * The relationship between the variables and the energy consumption of appliances is not well represented by the linear model       since the residuals are not normally distributed.
   

PORTFOLIO 3:

DATA: Generated random data points

OBJECTIVE: This notebook illustrates the process of K-means clustering by generating some random clusters of data and then showing the iterations of the algorithm as random cluster means are updated.

CONCLUSION:
Some of the most interesting findings in the dataset were:

  * The number of iteration needed to complete the k-means was 7












