
# Codebook

## Description of the raw data
The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data. 

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain. See 'features_info.txt' for more details. 

For each record it is provided:

- Triaxial acceleration from the accelerometer (total acceleration) and the estimated body acceleration.
- Triaxial Angular velocity from the gyroscope. 
- A 561-feature vector with time and frequency domain variables. 
- Its activity label. 
- An identifier of the subject who carried out the experiment.

## Files from the raw data
The following files from the folder `UCI HAR Dataset` were used in order to create the final `TidyDataSet.txt` file.

* `activity_labels.txt`
* `features.txt`
* `subject_train.txt`
* `X_train.txt`
* `y_train.txt`
* `subject_test.txt`
* `X_test.txt`
* `y_test.txt`

## Description of the variables in the tidy data set
The `TidyDataSet.txt` file contains:

* Identifier of the __subject__ who carried out the experiment(numbers `1-30`).
* The type of __activity__ in which the measurements took place(condition, i.e `WALKING`, `WALKING_UPSTAIRS`, etc).
* The average value of only the measurements of the mean and the standard deviation of each measurement, i.e the following measurements were included:
    + tBodyAcc-mean()-X
    + tBodyAcc-mean()-Y
    + tBodyAcc-mean()-Z
    + tBodyAcc-std()-X
    + tBodyAcc-std()-Y
    + tBodyAcc-std()-Z
    + tGravityAcc-mean()-X
    + tGravityAcc-mean()-Y
    + tGravityAcc-mean()-Z
    + tGravityAcc-std()-X
    + tGravityAcc-std()-Y
    + tGravityAcc-std()-Z
    + tBodyAccJerk-mean()-X
    + tBodyAccJerk-mean()-Y
    + tBodyAccJerk-mean()-Z
    + tBodyAccJerk-std()-X
    + tBodyAccJerk-std()-Y
    + tBodyAccJerk-std()-Z
    + tBodyGyro-mean()-X
    + tBodyGyro-mean()-Y
    + tBodyGyro-mean()-Z
    + tBodyGyro-std()-X
    + tBodyGyro-std()-Y
    + tBodyGyro-std()-Z
    + tBodyGyroJerk-mean()-X
    + tBodyGyroJerk-mean()-Y
    + tBodyGyroJerk-mean()-Z
    + tBodyGyroJerk-std()-X
    + tBodyGyroJerk-std()-Y
    + tBodyGyroJerk-std()-Z
    + tBodyAccMag-mean()
    + tBodyAccMag-std()
    + tGravityAccMag-mean()
    + tGravityAccMag-std()
    + tBodyAccJerkMag-mean()
    + tBodyAccJerkMag-std()
    + tBodyGyroMag-mean()
    + tBodyGyroMag-std()
    + tBodyGyroJerkMag-mean()
    + tBodyGyroJerkMag-std()
    + fBodyAcc-mean()-X
    + fBodyAcc-mean()-Y
    + fBodyAcc-mean()-Z
    + fBodyAcc-std()-X
    + fBodyAcc-std()-Y
    + fBodyAcc-std()-Z
    + fBodyAcc-meanFreq()-X
    + fBodyAcc-meanFreq()-Y
    + fBodyAcc-meanFreq()-Z
    + fBodyAccJerk-mean()-X
    + fBodyAccJerk-mean()-Y
    + fBodyAccJerk-mean()-Z
    + fBodyAccJerk-std()-X
    + fBodyAccJerk-std()-Y
    + fBodyAccJerk-std()-Z
    + fBodyAccJerk-meanFreq()-X
    + fBodyAccJerk-meanFreq()-Y
    + fBodyAccJerk-meanFreq()-Z
    + fBodyGyro-mean()-X
    + fBodyGyro-mean()-Y
    + fBodyGyro-mean()-Z
    + fBodyGyro-std()-X
    + fBodyGyro-std()-Y
    + fBodyGyro-std()-Z
    + fBodyGyro-meanFreq()-X
    + fBodyGyro-meanFreq()-Y
    + fBodyGyro-meanFreq()-Z
    + fBodyAccMag-mean()
    + fBodyAccMag-std()
    + fBodyAccMag-meanFreq()
    + fBodyBodyAccJerkMag-mean()
    + fBodyBodyAccJerkMag-std()
    + fBodyBodyAccJerkMag-meanFreq()
    + fBodyBodyGyroMag-mean()
    + fBodyBodyGyroMag-std()
    + fBodyBodyGyroMag-meanFreq()
    + fBodyBodyGyroJerkMag-mean()
    + fBodyBodyGyroJerkMag-std()
    + fBodyBodyGyroJerkMag-meanFreq()
    + angle(tBodyAccMean,gravity)
    + angle(tBodyAccJerkMean),gravityMean)
    + angle(tBodyGyroMean,gravityMean)
    + angle(tBodyGyroJerkMean,gravityMean)
    + angle(X,gravityMean)
    + angle(Y,gravityMean)
    + angle(Z,gravityMean)

***
**Note** that the raw data set in the __activity__ variables contained numbers from 1-6 in order to account for the condition in which each subject was measured. Hence, those numbers were replaced by their descriptive equivalents, i.e `WALKING` stands for `1`, `WALKING_UPSTAIRS` stands for `2` and so forth.
