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
 
