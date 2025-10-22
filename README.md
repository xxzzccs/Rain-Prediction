# Rain Prediction

Binary classification project to predict whether it will rain on a certain date given the past weather
data.

## Motivation

To explore ML workflows and understand binary classification models and their evaluation metrics.

## References for factors affecting rainfall

Gurumuda - <https://gurumuda.net/geography/factors-affecting-rainfall-in-an-area.html>

## Other Relevant Links for Reference

Google developers - <https://developers.google.com/machine-learning/crash-course/classification/accuracy-precision-recall>

## APIs Used

1. Historic Weather: "<https://historical-forecast-api.open-meteo.com/v1/forecast>"
2. Current Weather: "<https://api.open-meteo.com/v1/forecast>"

## Units in data set (as stated in the open meteo API documentation)

* date: ISO 8601
* temperature_2m: °C
* precipitation: mm
* rain: mm
* precipitation_probability: Percent (%)
* wind_speed_10m: kmph
* wind_direction_10m: degrees (°)
* surface_pressure: hPa

## Assumptions

When rain and precipitation is zero, the precipitation_probability should also be 0 for the given location of bangalore, India as there is no chance of snow.

## Learnings

Handling missing data is and thoroughly checking the data prior to model training is crucial for model performance.

## Conclusion

Dropping the rows with NaN values performed better likely due to the reduced ambiguity of the dataset, improving the model's ability to learn relationships between the features and targets.
Imputing also created ambiguity for the dataset causing the model to perform poorly.
