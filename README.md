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

## Submission File

For each site_path_timestamp row in the test set, you must predict the floor converted to an integer as per above and the x and y of the waypoint. 

The file should contain a header and have the following format:

      site_path_timestamp,floor,x,y
      5a0546857ecc773753327266_046cfa46be49fc10834815c6_1578474564146,0,15.0,55.0
      5a0546857ecc773753327266_046cfa46be49fc10834815c6_1578474573154,0,25.0,65.0
      5a0546857ecc773753327266_046cfa46be49fc10834815c6_1578474579463,0,35.0,75.0
      etc.


-------

## evaluation

Submissions are evaluated on the mean position error

IMPORTANT: The integer floor used in the submission must be mapped from the char/int floors used in the dataset. The mapping is as follows:

- F1, 1F  0

- F2, 2F  1

- etc.

- B1, 1B  -1

- B2, 2B  -2

There are other floor names in the training data, e.g., LG2, LM, etc., which you may decide to use for training, but none of these non-standard floors are found in the test set.


-------

## dataset
The dataset for this competition consists of dense indoor signatures of WiFi, geomagnetic field, iBeacons etc., as well as ground truth (waypoint) (locations) collected from hundreds of buildings in Chinese cities. 

The data found in path trace files (*.txt) corresponds to an indoor path between position p_1 and p_2 walked by a site-surveyor.

During the walk, an Android smartphone is held flat in front of the surveyors body, and a sensor data recording app is running on the device to collect IMU (accelerometer, gyroscope) and geomagnetic field (magnetometer) readings, as well as WiFi and Bluetooth iBeacon scanning results. 

A detailed description of the format of trace file is shown, along with other details and processing scripts, at this github link. 

In addition to raw trace files, floor plan metadata (e.g., raster image, size, GeoJSON) are also included for each floor.

A note on data quality: In the training files, you may find occasionally that a line is missing the ending newline character, causing it to run on to the next line. 

It is up to you how you want to handle this issue. This issue is not found in the test data.


### Files
- train: training path files, organized by site and floor; each path files contains the data of a single path on a single floor

- test: test path files, organized by site and floor; each path files contains the data of a single path on a single floor, but without the waypoint (x, y) data; the task of this competition is, for a given site-path file, predict the floor and waypoint locations at the timestamps given in the sample_submission.csv file

- metadata: floor metadata folder, organized by site and floor, which includes the following for each floor:
     
      floor_image.png
      floor_info.json
      geojson_map.json

- sample_submission.csv: a sample submission file in the correct format; each has a unique id which contains a site id, a path id, and the timestamp within the trace for which to make a prediction; see the Evaluation page for the required integer mapping of floor names

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

### Public Best LB Score: 4.470

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

## Postprocessing based on leakage
https://www.kaggle.com/c/hpa-single-cell-image-classification/leaderboard

      submission_df_leak_all.csv            LB 4.943   ver1
      
      submission_df_leak_end.csv            LB 4.755   ver1
      submission_df_leak_floor.csv          LB 4.995   ver1
      submission_df_leak_start.csv          LB 4.770   ver1
      
      submission_df_leak_start_end.csv      LB 4.737   ver1
      submission_df_leak_start_end.csv      LB 4.733   ver3   --- Best 


-------


## Postprocessing based on leakage-1


      submission_df_leak_all.csv            LB 4.924   ver3
      
      submission_df_leak_end.csv            LB 4.751   ver3
      submission_df_leak_floor.csv          LB 4.989   ver3
      submission_df_leak_start.csv          LB 4.750   ver3
      
      submission_df_leak_start_end.csv      LB 4.718   ver3


def unpickle(filename):

def to_pickle(filename, obj):


class FeatureStore():

class SiteInfo():



### train_meta_data

-------


## Ensembling best performing notebooks
https://www.kaggle.com/saurabhbagchi/ensembling-best-performing-notebooks

      LB: 4.744     ver7
      LB: 4.472     ver8 
      LB: 4.470     ver9     --- Best

-------


## Magn Cost Minimization + Post Processing
https://www.kaggle.com/mhilmiasyrofi/magn-cost-minimization-post-processing

      fs = 75    LB: 4.606     ver2
      fs = 100   LB: 4.519     ver1   --- default
      fs = 110   LB:     ver4    
      fs = 125   LB: 4.563     ver3
      
      
-------


      
