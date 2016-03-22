
Dataset Information

The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data.

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain. See 'features_info.txt' for more details.

For each record it is provided:
•	Triaxial acceleration from the accelerometer (total acceleration) and the estimated body acceleration.
•	Triaxial Angular velocity from the gyroscope.
•	A 561-feature vector with time and frequency domain variables.
•	Its activity label.
•	An identifier of the subject who carried out the experiment.

Study Design
The data was provided through the course project assignment.
All data and related files were moved from the self-contained folder UCI HAR Dataset to the data directory included in this repo.

The instruction was to
•	merge the training and test sets to create a single data set, and
•	to appropriately label the data set with description variable names.
Only collected the observations that met the project requirements.
Data was read into tables from the following files:
From ./data/train
•	X_train.txt
•	y_train.txt
•	subject_train.txt
From ./data/test
•	X_test.txt
•	y_test.txt
•	subject_test.txt
From ./data
•	features.txt
•	activity_labels.txt

Only mean() and std() variables were extracted from the train and test data sets. Additional “Mean” angle variables were excluded for the following reasons:
1.	they were not determined to be raw signal data, but were instead readings that were obtained by processing the original signal data
2.	and other readings within the original signal set in addition to mean() and std() were used to create the additional “Mean” values, which introduces additional data that was to be excluded from the tide data set.
The variables that were excluded that also included the word “Mean” were: gravityMean, tBodyAccMean, tBodyAccJerkMean,tBodyGyroMean, tBodyGyroJerkMean
Test and train internal signal data were excluded.
The original data can be downloaded here.

Code Book
The list of variables names with original variable names in italics, where applicable. Variable labels were modified from the original to improve readability.
Subject
The identifier for each subject who performed the activity for each window sample. Its range is from 1 to 30.
Activity
The name of the activity performed during the reading.
timeBodyAcc-Mean-X tBodyAcc-mean()-X
timeBodyAcc-Mean-Y tBodyAcc-mean()-Y
timeBodyAcc-Mean-Z tBodyAcc-mean()-Z
3-axial time domain body acceleration signals - mean value
timeBodyAcc-StdDev-X tBodyAcc-std()-X
timeBodyAcc-StdDev-Y tBodyAcc-std()-Y
timeBodyAcc-StdDev-Z tBodyAcc-std()-Z
3-axial time domain body acceleration signals - standard deviation
timeGravityAcc-Mean-X tGravityAcc-mean()-X
timeGravityAcc-Mean-Y tGravityAcc-mean()-Y
timeGravityAcc-Mean-Z tGravityAcc-mean()-Z
3-axial time domain gravity acceleration signals - mean value
timeGravityAcc-StdDev-X tGravityAcc-std()-X
timeGravityAcc-StdDev-Y tGravityAcc-std()-Y
timeGravityAcc-StdDev-Z tGravityAcc-std()-Z
3-axial time domain gravity acceleration signals - standard deviation
timeBodyAccJerk-Mean-X tBodyAccJerk-mean()-X
timeBodyAccJerk-Mean-Y tBodyAccJerk-mean()-Y
timeBodyAccJerk-Mean-Z tBodyAccJerk-mean()-Z
3-axial time domain accelerometer Jerk signals - mean value
timeBodyAccJerk-StdDev-X tBodyAccJerk-std()-X
timeBodyAccJerk-StdDev-Y tBodyAccJerk-std()-Y
timeBodyAccJerk-StdDev-Z tBodyAccJerk-std()-Z
3-axial time domain body accelerometer Jerk signals - standard deviation
timeBodyGyro-Mean-X tBodyGyro-mean()-X
timeBodyGyro-Mean-Y tBodyGyro-mean()-Y
timeBodyGyro-Mean-Z tBodyGyro-mean()-Z
3-axial time domain body gyroscope signals - mean value
timeBodyGyro-StdDev-X tBodyGyro-std()-X
timeBodyGyro-StdDev-Y tBodyGyro-std()-Y
timeBodyGyro-StdDev-Z tBodyGyro-std()-Z
3-axial time domain body gyroscope Jerk signals - standard deviation
timeBodyGyroJerk-Mean-X tBodyGyroJerk-mean()-X
timeBodyGyroJerk-Mean-Y tBodyGyroJerk-mean()-Y
timeBodyGyroJerk-Mean-Z tBodyGyroJerk-mean()-Z
3-axial time domain body gyroscope Jerk signals - mean value
timeBodyGyroJerk-StdDev-X tBodyGyroJerk-std()-X
timeBodyGyroJerk-StdDev-Y tBodyGyroJerk-std()-Y
timeBodyGyroJerk-StdDev-Z tBodyGyroJerk-std()-Z
3-axial time domain body gyroscope Jerk signals - standard deviation
timeBodyAccMag-Mean tBodyAccMag-mean()
Time domain body accelerometer magnitude, calculated using the Euclidean norm - mean value
timeBodyAccMag-StdDev tBodyAccMag-std()
Time domain body accelerometer magnitude, calculated using the Euclidean norm - standard deviation
timeGravityAccMag-Mean tGravityAccMag-mean()
Time domain gravity accelerometer magnitude, calculated using the Euclidean norm - mean value
timeGravityAccMag-StdDev tGravityAccMag-std()
Time domain body accelerometer magnitude, calculated using the Euclidean norm - standard deviation
timeBodyAccJerkMag-Mean tBodyAccJerkMag-mean()
Time domain body accelerometer Jerk magnitude, calculated using the Euclidean norm - mean value
timeBodyAccJerkMag-StdDev tBodyAccJerkMag-std()
Time domain body accelerometer Jerk magnitude, calculated using the Euclidean norm - standard deviation
timeBodyGyroMag-Mean tBodyGyroMag-mean()
Time domain body gyroscope magnitude, calculated using the Euclidean norm - mean value
timeBodyGyroMag-StdDev tBodyGyroMag-std()
Time domain body gyroscope magnitude, calculated using the Euclidean norm - standard deviation
timeBodyGyroJerkMag-Mean tBodyGyroJerkMag-mean()
Time domain body gyroscope Jerk magnitude, calculated using the Euclidean norm - mean value
timeBodyGyroJerkMag-StdDev tBodyGyroJerkMag-std()
Time domain body gyroscope Jerk magnitude, calculated using the Euclidean norm - standard deviation
freqBodyAcc-Mean-X fBodyAcc-mean()-X
freqBodyAcc-Mean-Y fBodyAcc-mean()-Y
freqBodyAcc-Mean-Z fBodyAcc-mean()-Z
3-axial frequency domain body acceleration signals - mean value
freqBodyAcc-StdDev-X fBodyAcc-std()-X
freqBodyAcc-StdDev-Y fBodyAcc-std()-Y
freqBodyAcc-StdDev-Z fBodyAcc-std()-Z
3-axial frequency domain body acceleration signals - standard deviation
freqBodyAccJerk-Mean-X fBodyAccJerk-mean()-X
freqBodyAccJerk-Mean-Y fBodyAccJerk-mean()-Y
freqBodyAccJerk-Mean-Z fBodyAccJerk-mean()-Z
3-axial frequency domain body acceleration Jerk signals - mean value
freqBodyAccJerk-StdDev-X fBodyAccJerk-std()-X
freqBodyAccJerk-StdDev-Y fBodyAccJerk-std()-Y
freqBodyAccJerk-StdDev-Z fBodyAccJerk-std()-Z
3-axial frequency domain body acceleration Jerk signals - standard deviation
freqBodyGyro-Mean-X fBodyGyro-mean()-X
freqBodyGyro-Mean-Y fBodyGyro-mean()-Y
freqBodyGyro-Mean-Z fBodyGyro-mean()-Z
3-axial frequency domain body gyroscope signals - mean value
freqBodyGyro-StdDev-X fBodyGyro-std()-X
freqBodyGyro-StdDev-Y fBodyGyro-std()-Y
freqBodyGyro-StdDev-Z fBodyGyro-std()-Z
3-axial frequency domain body gyroscope signals - standard deviation
freqBodyAccMag-Mean fBodyAccMag-mean()
Frequency domain body accelerometer magnitude - mean value
freqBodyAccMag-StdDev fBodyAccMag-std()
Frequency domain body accelerometer magnitude - standard deviation
freqBodyAccJerkMag-Mean fBodyBodyAccJerkMag-mean()
Frequency domain body accelerometer Jerk magnitude - mean value
freqBodyAccJerkMag-StdDev fBodyBodyAccJerkMag-std()
Frequency domain body accelerometer Jerk magnitude - standard deviation
freqBodyGyroMag-Mean fBodyBodyGyroMag-mean()
Frequency domain body gyroscope magnitude - mean value
freqBodyGyroMag-StdDev fBodyBodyGyroMag-std()
Frequency domain body gyroscope magnitude - standard deviation
freqBodyGyroJerkMag-Mean fBodyBodyGyroJerkMag-mean()
Frequency domain body gyroscope Jerk magnitude - mean value
freqBodyGyroJerkMag-StdDev fBodyBodyGyroJerkMag-std()
Frequency domain body gyroscope Jerk magnitude - standard deviation
________________________________________
NOTE: Fast Fourier Transform (FFT) was applied frequency domain signals

