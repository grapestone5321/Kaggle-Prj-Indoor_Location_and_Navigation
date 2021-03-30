# Kaggle Indoor Location & Navigation

Identify the position of a smartphone in a shopping mall


-------

## submission deadline
May 17, 2021 - Final submission deadline at 11:59 PM UTC 


-------

## task
 your task is to predict the indoor position of smartphones based on real-time sensor data, provided by indoor positioning technology company XYZ10 in partnership with Microsoft Research. 
 
 You'll locate devices using “active” localization data, which is made available with the cooperation of the user. 
 
 Unlike passive localization methods (e.g. radar, camera), the data provided for this competition requires explicit user permission. 
 
 You'll work with a dataset of nearly 30,000 traces from over 200 buildings.


-------

## evaluation

Submissions are evaluated on the mean position error

-------

## dataset
The dataset for this competition consists of dense indoor signatures of WiFi, geomagnetic field, iBeacons etc., as well as ground truth (waypoint) (locations) collected from hundreds of buildings in Chinese cities. 

The data found in path trace files (*.txt) corresponds to an indoor path between position p_1 and p_2 walked by a site-surveyor.

During the walk, an Android smartphone is held flat in front of the surveyors body, and a sensor data recording app is running on the device to collect IMU (accelerometer, gyroscope) and geomagnetic field (magnetometer) readings, as well as WiFi and Bluetooth iBeacon scanning results. 

A detailed description of the format of trace file is shown, along with other details and processing scripts, at this github link. 

In addition to raw trace files, floor plan metadata (e.g., raster image, size, GeoJSON) are also included for each floor.

A note on data quality: In the training files, you may find occasionally that a line is missing the ending newline character, causing it to run on to the next line. 

It is up to you how you want to handle this issue. This issue is not found in the test data.

-------

## github link
### location-competition/indoor-location-competition-20
https://github.com/location-competition/indoor-location-competition-20



-------

## Webinar
### Indoor Location Competition 2.0 Webinar
https://www.youtube.com/watch?v=xt3OzMC-XMU

## References:
https://developer.android.com/guide/topics/sensors
https://developer.android.com/reference/android/net/wifi/ScanResult.html
https://developer.android.com/reference/android/bluetooth/le/ScanRecord

-------

## Progress

### Public Best LB Score: 7.745

### Private Score: 


-------

## multi-task-mlp[Inference]
https://www.kaggle.com/a763337092/multi-task-mlp-inference




## wifi features lightgbm starter
https://www.kaggle.com/devinanzelmo/wifi-features-lightgbm-starter



## Indoor GBM+postprocessing XY prediction


### 'learning_rate': 0.1, #default=0.1

      'learning_rate': 0.1       LB 7.745   ver1   --- Best 
      'learning_rate': 0.01      LB         ver2
    
    
    
-------





