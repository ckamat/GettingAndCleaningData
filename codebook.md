---
title: "CodeBook for the Getting and Cleaning Data Project"
author: "Chetan Kamat"
date: "26 July 2015"
output: html_document
---

# Getting and Cleaning Data Project

## Description

Additional information about the variables, data and transformations used in the course project for the Johns Hopkins Getting and Cleaning Data course.
Source Data

A full description of the data used in this project can be found at The UCI Machine Learning Repository

The source data for this project can be found here.
[Data Set Information] (https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip )


##Attribute Information

For each record in the dataset it is provided:

* Triaxial acceleration from the accelerometer (total acceleration) and the estimated body acceleration.
* Triaxial Angular velocity from the gyroscope.
* A 561-feature vector with time and frequency domain variables.
* Its activity label.
* An identifier of the subject who carried out the experiment.

#### Section 1. Merge the training and the test sets to create one data set.

After setting the source directory for the files, read into tables the data located in

    1. features.txt
    2. activity_labels.txt
    3. subject_train.txt
    4. x_train.txt
    5. y_train.txt
    6. subject_test.txt
    7. x_test.txt
    8. y_test.txt

Assign column names and merge to create one data set.

#### Section 2. Extract only the measurements on the mean and standard deviation for each measurement.

Create a logcal vector that contains TRUE values for the ID, mean and stdev columns and FALSE values for the others. Subset this data to keep only the necessary columns.
Create a logical vector that contains TRUE values for the ID, mean and stdev columns and FALSE values for the others. Subset this data to keep only the necessary columns.

#### Section 3. Use descriptive activity names to name the activities in the data set

Merge data subset with the activityType table to inlude the descriptive activity names

#### Section 4. Appropriately label the data set with descriptive activity names.

Use gsub function for pattern replacement to clean up the data labels.

#### Section 5. Create a second, independent tidy data set with the average of each variable for each activity and each subject.

Per the project instructions, we need to produce only a data set with the average of each variable for each activity and subject. 
As per the instruction the output has been generated (tidydata.txt) with the write.table() function using row.name=FALSE parameter. 



