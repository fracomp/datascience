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


