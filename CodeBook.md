 Merge the training and the test sets to create one data set.
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

Changing variable names to something meaningful:
new column names:
[1] "tBodyAccelerationmeanX"                             
 [2] "tBodyAccelerationmeanY"                             
 [3] "tBodyAccelerationmeanZ"                             
 [4] "tGravityAccelerationmeanX"                          
 [5] "tGravityAccelerationmeanY"                          
 [6] "tGravityAccelerationmeanZ"                          
 [7] "tBodyAccelerationJerkmeanX"                         
 [8] "tBodyAccelerationJerkmeanY"                         
 [9] "tBodyAccelerationJerkmeanZ"                         
[10] "tBodyGyroscopemeanX"                                
[11] "tBodyGyroscopemeanY"                                
[12] "tBodyGyroscopemeanZ"                                
[13] "tBodyGyroscopeJerkmeanX"                            
[14] "tBodyGyroscopeJerkmeanY"                            
[15] "tBodyGyroscopeJerkmeanZ"                            
[16] "tBodyAccelerationMagnitudemean"                     
[17] "tGravityAccelerationMagnitudemean"                  
[18] "tBodyAccelerationJerkMagnitudemean"                 
[19] "tBodyGyroscopeMagnitudemean"                        
[20] "tBodyGyroscopeJerkMagnitudemean"                    
[21] "fBodyAccelerationmeanX"                             
[22] "fBodyAccelerationmeanY"                             
[23] "fBodyAccelerationmeanZ"                             
[24] "fBodyAccelerationJerkmeanX"                         
[25] "fBodyAccelerationJerkmeanY"                         
[26] "fBodyAccelerationJerkmeanZ"                         
[27] "fBodyGyroscopemeanX"                                
[28] "fBodyGyroscopemeanY"                                
[29] "fBodyGyroscopemeanZ"                                
[30] "fBodyAccelerationMagnitudemean"                     
[31] "fBodyBodyAccelerationJerkMagnitudemean"             
[32] "fBodyBodyGyroscopeMagnitudemean"                    
[33] "fBodyBodyGyroscopeJerkMagnitudemean"                
[34] "tBodyAccelerationstandarddeviationX"                
[35] "tBodyAccelerationstandarddeviationY"                
[36] "tBodyAccelerationstandarddeviationZ"                
[37] "tGravityAccelerationstandarddeviationX"             
[38] "tGravityAccelerationstandarddeviationY"             
[39] "tGravityAccelerationstandarddeviationZ"             
[40] "tBodyAccelerationJerkstandarddeviationX"            
[41] "tBodyAccelerationJerkstandarddeviationY"            
[42] "tBodyAccelerationJerkstandarddeviationZ"            
[43] "tBodyGyroscopestandarddeviationX"                   
[44] "tBodyGyroscopestandarddeviationY"                   
[45] "tBodyGyroscopestandarddeviationZ"                   
[46] "tBodyGyroscopeJerkstandarddeviationX"               
[47] "tBodyGyroscopeJerkstandarddeviationY"               
[48] "tBodyGyroscopeJerkstandarddeviationZ"               
[49] "tBodyAccelerationMagnitudestandarddeviation"        
[50] "tGravityAccelerationMagnitudestandarddeviation"     
[51] "tBodyAccelerationJerkMagnitudestandarddeviation"    
[52] "tBodyGyroscopeMagnitudestandarddeviation"           
[53] "tBodyGyroscopeJerkMagnitudestandarddeviation"       
[54] "fBodyAccelerationstandarddeviationX"                
[55] "fBodyAccelerationstandarddeviationY"                
[56] "fBodyAccelerationstandarddeviationZ"                
[57] "fBodyAccelerationJerkstandarddeviationX"            
[58] "fBodyAccelerationJerkstandarddeviationY"            
[59] "fBodyAccelerationJerkstandarddeviationZ"            
[60] "fBodyGyroscopestandarddeviationX"                   
[61] "fBodyGyroscopestandarddeviationY"                   
[62] "fBodyGyroscopestandarddeviationZ"                   
[63] "fBodyAccelerationMagnitudestandarddeviation"        
[64] "fBodyBodyAccelerationJerkMagnitudestandarddeviation"
[65] "fBodyBodyGyroscopeMagnitudestandarddeviation"       
[66] "fBodyBodyGyroscopeJerkMagnitudestandarddeviation"   
[67] "activity"                                           
[68] "subject" 
