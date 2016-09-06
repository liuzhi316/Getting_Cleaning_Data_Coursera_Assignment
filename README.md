## Introduction.

###  The data linked to from the course website represent data collected from the accelerometers from the Samsung Galaxy S smartphone. The R script run_analysis.R here does the following:
* Merges the training and the test sets to create one data set.
* Extracts only the measurements on the mean and standard deviation for each measurement.
* Uses descriptive activity names to name the activities in the data set
* Appropriately labels the data set with descriptive variable names.
* From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.


## Loading data.

### the data from train and test folder were loaded to the R environment:

setwd("./UCI HAR Dataset")
features <- read.delim("features.txt", sep = "", header = F)
setwd("./train")
x_train <- read.delim("x_train.txt", sep = "", header = F)
y_train <- read.delim("y_train.txt", sep = "", header = F)
subject_train <- read.delim("subject_train.txt", sep = "", header = F)

setwd("../test")
x_test <- read.delim("x_test.txt", sep = "", header = F)
y_test <- read.delim("y_test.txt", sep = "", header = F)
subject_test <- read.delim("subject_test.txt", sep = "", header = F)



## Extracting columns.

### only the measurements on the mean and standard deviation for each measurement were extreacted. (Note: "meanFreq()" was not included because it's not the parameter required here.)

newcol <- grep("mean\\(\\)|std\\(\\)", features$V2)
x_train_new <- x_train[, newcol]
colnames(x_train_new) <- features$V2[newcol]
x_test_new <- x_test[, newcol]
colnames(x_test_new) <- features$V2[newcol]


## Merge and rename the columns.

### train and test data were renamed first and then merged together.

new_train <- data.frame(subject_train, y_train, x_train_new)
names(new_train)[1] <- "volunteer_ID"
names(new_train)[2] <- "Activity"
new_train$Activity[new_train$Activity=="1"] <- "WALKING"
new_train$Activity[new_train$Activity=="2"] <- "WALKING_UPSTAIRS"
new_train$Activity[new_train$Activity=="3"] <- "WALKING_DOWNSTAIRS"
new_train$Activity[new_train$Activity=="4"] <- "SITTING"
new_train$Activity[new_train$Activity=="5"] <- "STANDING"
new_train$Activity[new_train$Activity=="6"] <- "LAYING"

new_test <- data.frame(subject_test, y_test, x_test_new)
names(new_test)[1] <- "volunteer_ID"
names(new_test)[2] <- "Activity"
new_test$Activity[new_test$Activity=="1"] <- "WALKING"
new_test$Activity[new_test$Activity=="2"] <- "WALKING_UPSTAIRS"
new_test$Activity[new_test$Activity=="3"] <- "WALKING_DOWNSTAIRS"
new_test$Activity[new_test$Activity=="4"] <- "SITTING"
new_test$Activity[new_test$Activity=="5"] <- "STANDING"
new_test$Activity[new_test$Activity=="6"] <- "LAYING"

newdata <- rbind(new_test, new_train)


## making the final dataset.

### the average of each variable for each activity and each subject

finaldataset <- aggregate(newdata[,c(-1,-2)], list(newdata$volunteer_ID, newdata$Activity), mean)
names(finaldataset)[1] <- "volunteer_ID"
names(finaldataset)[2] <- "Activity"
write.csv(finaldataset, file = "finaldataset.csv")
 