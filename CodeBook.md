## UCI HAR Dataset -- final dataset

### The features selected for this database come from the accelerometer and gyroscope 3-axial raw signals tAcc-XYZ and tGyro-XYZ. These time domain signals (prefix 't' to denote time) were captured at a constant rate of 50 Hz. Then they were filtered using a median filter and a 3rd order low pass Butterworth filter with a corner frequency of 20 Hz to remove noise. Similarly, the acceleration signal was then separated into body and gravity acceleration signals (tBodyAcc-XYZ and tGravityAcc-XYZ) using another low pass Butterworth filter with a corner frequency of 0.3 Hz. 
Subsequently, the body linear acceleration and angular velocity were derived in time to obtain Jerk signals (tBodyAccJerk-XYZ and tBodyGyroJerk-XYZ). Also the magnitude of these three-dimensional signals were calculated using the Euclidean norm (tBodyAccMag, tGravityAccMag, tBodyAccJerkMag, tBodyGyroMag, tBodyGyroJerkMag). Finally a Fast Fourier Transform (FFT) was applied to some of these signals producing fBodyAcc-XYZ, fBodyAccJerk-XYZ, fBodyGyro-XYZ, fBodyAccJerkMag, fBodyGyroMag, fBodyGyroJerkMag. (Note the 'f' to indicate frequency domain signals). 
These signals were used to estimate variables of the feature vector for each pattern: '-XYZ' is used to denote 3-axial signals in the X, Y and Z directions.

### This dataset was extracted from the original train and test dataset and only the measurements on the mean and standard deviation for each measurement were included.


3) a code book that describes the variables, the data, and any transformations or work that you performed to clean up the data called CodeBook.md.
code book that modifies and updates the available codebooks with the data to indicate all the variables and summaries calculated, along with units, and any other relevant information.




Column 1. Volunteer_ID
  1:30

Column 2. Activity
  1 WALKING
2 WALKING_UPSTAIRS
3 WALKING_DOWNSTAIRS
4 SITTING
5 STANDING
6 LAYING


column 3. tBodyAcc-mean()-X

column 4. tBodyAcc-mean()-Y

column 5. tBodyAcc-mean()-Z

column 6. tBodyAcc-std()-X

column 7. tBodyAcc-std()-Y

column 8. tBodyAcc-std()-Z

column 9. tGravityAcc-mean()-X

column 10. tGravityAcc-mean()-Y

column 11. tGravityAcc-mean()-Z

column 12. tGravityAcc-std()-X

column 13. tGravityAcc-std()-Y

column 14. tGravityAcc-std()-Z

column 15. tBodyAccJerk-mean()-X

column 16. tBodyAccJerk-mean()-Y

column 17. tBodyAccJerk-mean()-Z

column 18. tBodyAccJerk-std()-X

column 19. tBodyAccJerk-std()-Y

column 20. tBodyAccJerk-std()-Z

column 21. tBodyGyro-mean()-X

column 22. tBodyGyro-mean()-Y

column 23. tBodyGyro-mean()-Z

column 24. tBodyGyro-std()-X

column 25. tBodyGyro-std()-Y

column 26. tBodyGyro-std()-Z

column 27. tBodyGyroJerk-mean()-X

column 28. tBodyGyroJerk-mean()-Y

column 29. tBodyGyroJerk-mean()-Z

column 30. tBodyGyroJerk-std()-X

column 31. tBodyGyroJerk-std()-Y

column 32. tBodyGyroJerk-std()-Z

column 33. tBodyAccMag-mean()

column 34. tBodyAccMag-std()

column 35. tGravityAccMag-mean()

column 36. tGravityAccMag-std()

column 37. tBodyAccJerkMag-mean()

column 38. tBodyAccJerkMag-std()

column 39. tBodyGyroMag-mean()

column 40. tBodyGyroMag-std()

column 41. tBodyGyroJerkMag-mean()

column 42. tBodyGyroJerkMag-std()

column 43. fBodyAcc-mean()-X

column 44. fBodyAcc-mean()-Y

column 45. fBodyAcc-mean()-Z

column 46. fBodyAcc-std()-X

column 47. fBodyAcc-std()-Y

column 48. fBodyAcc-std()-Z

column 49. fBodyAccJerk-mean()-X

column 50. fBodyAccJerk-mean()-Y

column 51. fBodyAccJerk-mean()-Z

column 52. fBodyAccJerk-std()-X

column 53. fBodyAccJerk-std()-Y

column 54. fBodyAccJerk-std()-Z

column 55. fBodyGyro-mean()-X

column 56. fBodyGyro-mean()-Y

column 57. fBodyGyro-mean()-Z

column 58. fBodyGyro-std()-X

column 59. fBodyGyro-std()-Y

column 60. fBodyGyro-std()-Z

column 61. fBodyAccMag-mean()

column 62. fBodyAccMag-std()

column 63. fBodyBodyAccJerkMag-mean()

column 64. fBodyBodyAccJerkMag-std()

column 65. fBodyBodyGyroMag-mean()

column 66. fBodyBodyGyroMag-std()

column 67. fBodyBodyGyroJerkMag-mean()

column 68. fBodyBodyGyroJerkMag-std()
