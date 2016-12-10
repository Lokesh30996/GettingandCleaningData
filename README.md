#Merges the training and the test sets to create one data set.

Initially, it reads the training and test data and merges them into one data table. It reads the data from each of "test" and "train" folder. This process occurs independently for each of "x","subj","y" variable.

#Extracts only the measurements on the mean and standard deviation for each measurement.

We read features data. Using pattern matching, we find all the feature names which have either "mean" or "std" in it and only extract those column indexes from our "x" dataset.

#Uses descriptive activity names to name the activities in the data set

In "x" dataset, we rename the columns using the names from "features" data frame. In addition we also convert all the names to lower case and remove any "(" or ")" characters. In addition to that we also read activities from activity_labels file and do all the text pre formatting and then merge those names as the column names of "y" data table.

#Appropriately labels the data set with descriptive variable names.

We now merge all the 3 data tables and as its a properly formatted data we write it into "merged.txt" file.

#From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.

We find the mean based on activity and subject variables. And hence we have our average values data set also which is written onto disk as "average.txt".