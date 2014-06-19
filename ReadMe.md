 1.run_analysis.R is divided into 5 blocks, based on questions asked in the assignment.
 2.The output from each block is provided as input to the next block.
 3.To see the final output saved as a csv file, run the script all at once by providing  appropriate paths for input and output files.

Processing Steps :
1. Load xtest,test into two separate data frames.
2. combine them using Cbind.
3. Load strain,train into two separate data frames.
4. combine them using Cbind.
Combining Test and Train Observations:
5. combine result from 2 and 4 using rbind.

Naming columns:
1. Obtain column names from “features.txt”.
2. Assign column names to the result in step 5 from above.
3. Add two new Columns to the data set(activity, subject)

Subsetting(Extracting only those measurements that has mean() and std():
1. Extract desired columns by using Regex grep("mean\\(\\)", features$V2) and grep("std\\(\\)", features$V2).
2. Add descriptive names to activity column from activity_labels.txt.

Rename Column Names:

 Creates a second, independent tidy data set with the average of each variable for each activity and each subject using melt and cast functions.