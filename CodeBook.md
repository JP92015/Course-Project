# Assignment: Getting and Cleaning Data Course Project
Getting and Cleaning Data Course Project

run_analysis contains a script to load test and training data from the UCI HAR Dataset, compute means by activity and subject
from reported variable means, and returns this data in tidy format.

run_analysis() consists of subfunctions to acheive these tasks:
 library(dplyr) loads the dplyr package, which the script requires.
 
 loadTrainingData() loads training data from the UCI HAR Dataset, merging variable data with activity label and subject
 
 loadTestingData() loads testing data from the UCI HAR Dataset, merging variable data with activity label and subject
 
 combineSelectAndDescribe() combines training and testing datasets, subsets out variable mean and standard deviation data,
  and merges activity descriptions with activity labels
 
 findAverageByGroups() finds the mean for each Subject in each Activity
 
 tidyData() presents the results in tidy data format- one observation per row, one variable per column
 
 
 Variable information is given in the UCI HAR Dataset, repeated here:
 
 "The features selected for this database come from the accelerometer and gyroscope 3-axial raw signals tAcc-XYZ and tGyro-XYZ. These time domain signals (prefix 't' to denote time) were captured at a constant rate of 50 Hz. Then they were filtered using a median filter and a 3rd order low pass Butterworth filter with a corner frequency of 20 Hz to remove noise. Similarly, the acceleration signal was then separated into body and gravity acceleration signals (tBodyAcc-XYZ and tGravityAcc-XYZ) using another low pass Butterworth filter with a corner frequency of 0.3 Hz. 

Subsequently, the body linear acceleration and angular velocity were derived in time to obtain Jerk signals (tBodyAccJerk-XYZ and tBodyGyroJerk-XYZ). Also the magnitude of these three-dimensional signals were calculated using the Euclidean norm (tBodyAccMag, tGravityAccMag, tBodyAccJerkMag, tBodyGyroMag, tBodyGyroJerkMag). 

Finally a Fast Fourier Transform (FFT) was applied to some of these signals producing fBodyAcc-XYZ, fBodyAccJerk-XYZ, fBodyGyro-XYZ, fBodyAccJerkMag, fBodyGyroMag, fBodyGyroJerkMag. (Note the 'f' to indicate frequency domain signals). 

These signals were used to estimate variables of the feature vector for each pattern:  
'-XYZ' is used to denote 3-axial signals in the X, Y and Z directions.

tBodyAcc-XYZ

tGravityAcc-XYZ

tBodyAccJerk-XYZ

tBodyGyro-XYZ

tBodyGyroJerk-XYZ

tBodyAccMag

tGravityAccMag

tBodyAccJerkMag

tBodyGyroMag

tBodyGyroJerkMag

fBodyAcc-XYZ

fBodyAccJerk-XYZ

fBodyGyro-XYZ

fBodyAccMag

fBodyAccJerkMag

fBodyGyroMag

fBodyGyroJerkMag"



Mean and Standard Deviation values were then calculated and given in the UCI HAR Dataset. These were extracted for the present analysis. The mean of these mean and standard deviation values were then calculated for each participate undertaking each activity. This is reported in the resulting dataset.
