#Creating the training data frame
#reading the features
features <- read.table("features.txt", sep="", header= FALSE, as.is = TRUE)[,2]
#reading the training X_train data and assigning features to the col.names attribute
x_train <- read.table("./train/X_train.txt",sep = "",header = FALSE, as.is = TRUE, col.names = features)
#reading the activity codes
y_train <-read.table("train/y_train.txt",sep="", header=FALSE)
#reading the activity labels
labels <- read.table("activity_labels.txt",sep="",header=FALSE, col.names = c("activity_id", "activity_label"))
#transforming the y_train to contain the activity labels instead of their ids
y_train <- apply(y_train,1,function (x) labels[x,2])
#transforming it to dataframe and setting column names
y_train <- as.data.frame(y_train)
colnames(y_train) <- "activity"
#reading subjects id
subjects <- read.table("train/subject_train.txt", sep="", header = FALSE, col.names = "subject_id")


#Reading Inertial Signals
# body acc
#we first create the labels
body_acc_x_labels <- paste("body_acc_x",seq(1,128,1), sep="_")
body_acc_x_train <- read.table("train/Inertial Signals/body_acc_x_train.txt", header = FALSE, col.names =body_acc_x_labels)
body_acc_y_labels <- paste("body_acc_y",seq(1,128,1), sep="_")
body_acc_y_train <- read.table("train/Inertial Signals/body_acc_y_train.txt", header = FALSE, col.names =body_acc_y_labels)
body_acc_z_labels <- paste("body_acc_z",seq(1,128,1), sep="_")
body_acc_z_train <- read.table("train/Inertial Signals/body_acc_z_train.txt", header = FALSE, col.names =body_acc_z_labels)


# body gyro
#we first create the labels
body_gyro_x_labels <- paste("body_gyro_x",seq(1,128,1), sep="_")
body_gyro_x_train <- read.table("train/Inertial Signals/body_gyro_x_train.txt", header = FALSE, col.names =body_gyro_x_labels)
body_gyro_y_labels <- paste("body_gyro_y",seq(1,128,1), sep="_")
body_gyro_y_train <- read.table("train/Inertial Signals/body_gyro_y_train.txt", header = FALSE, col.names =body_gyro_y_labels)
body_gyro_z_labels <- paste("body_gyro_z",seq(1,128,1), sep="_")
body_gyro_z_train <- read.table("train/Inertial Signals/body_gyro_z_train.txt", header = FALSE, col.names =body_gyro_z_labels)

#total_acc
#we first create the labels
total_acc_x_labels <- paste("total_acc_x",seq(1,128,1), sep="_")
total_acc_x_train <- read.table("train/Inertial Signals/total_acc_x_train.txt", header = FALSE, col.names =total_acc_x_labels)
total_acc_y_labels <- paste("total_acc_y",seq(1,128,1), sep="_")
total_acc_y_train <- read.table("train/Inertial Signals/total_acc_y_train.txt", header = FALSE, col.names =total_acc_y_labels)
total_acc_z_labels <- paste("total_acc_z",seq(1,128,1), sep="_")
total_acc_z_train <- read.table("train/Inertial Signals/total_acc_z_train.txt", header = FALSE, col.names =total_acc_z_labels)

# finnally :  creating the training set
#merging the three data frames
train <- cbind(subjects,y_train, x_train,
               body_acc_x_train,
               body_acc_y_train,
               body_acc_z_train,
               body_gyro_x_train,
               body_gyro_y_train,
               body_gyro_z_train,
               total_acc_x_train,
               total_acc_y_train,
               total_acc_z_train)

#now we do the same for the test data

#Creating the testing data frame
#reading the testing X_test data and assigning features to the col.names attribute
x_test <- read.table("./test/X_test.txt",sep = "",header = FALSE, as.is = TRUE, col.names = features)
#reading the activity codes
y_test <-read.table("test/y_test.txt",sep="", header=FALSE)
#reading the activity labels
labels <- read.table("activity_labels.txt",sep="",header=FALSE, col.names = c("activity_id", "activity_label"))
#transforming the y_test to contain the activity labels instead of their ids
y_test <- apply(y_test,1,function (x) labels[x,2])
#transforming it to dataframe and setting column names
y_test <- as.data.frame(y_test)
colnames(y_test) <- "activity"
#reading subjects id
subjects <- read.table("test/subject_test.txt", sep="", header = FALSE, col.names = "subject_id")


#Reading Inertial Signals
# body acc
#we first create the labels
body_acc_x_labels <- paste("body_acc_x",seq(1,128,1), sep="_")
body_acc_x_test <- read.table("test/Inertial Signals/body_acc_x_test.txt", header = FALSE, col.names =body_acc_x_labels)
body_acc_y_labels <- paste("body_acc_y",seq(1,128,1), sep="_")
body_acc_y_test <- read.table("test/Inertial Signals/body_acc_y_test.txt", header = FALSE, col.names =body_acc_y_labels)
body_acc_z_labels <- paste("body_acc_z",seq(1,128,1), sep="_")
body_acc_z_test <- read.table("test/Inertial Signals/body_acc_z_test.txt", header = FALSE, col.names =body_acc_z_labels)


# body gyro
#we first create the labels
body_gyro_x_labels <- paste("body_gyro_x",seq(1,128,1), sep="_")
body_gyro_x_test <- read.table("test/Inertial Signals/body_gyro_x_test.txt", header = FALSE, col.names =body_gyro_x_labels)
body_gyro_y_labels <- paste("body_gyro_y",seq(1,128,1), sep="_")
body_gyro_y_test <- read.table("test/Inertial Signals/body_gyro_y_test.txt", header = FALSE, col.names =body_gyro_y_labels)
body_gyro_z_labels <- paste("body_gyro_z",seq(1,128,1), sep="_")
body_gyro_z_test <- read.table("test/Inertial Signals/body_gyro_z_test.txt", header = FALSE, col.names =body_gyro_z_labels)

#total_acc
#we first create the labels
total_acc_x_labels <- paste("total_acc_x",seq(1,128,1), sep="_")
total_acc_x_test <- read.table("test/Inertial Signals/total_acc_x_test.txt", header = FALSE, col.names =total_acc_x_labels)
total_acc_y_labels <- paste("total_acc_y",seq(1,128,1), sep="_")
total_acc_y_test <- read.table("test/Inertial Signals/total_acc_y_test.txt", header = FALSE, col.names =total_acc_y_labels)
total_acc_z_labels <- paste("total_acc_z",seq(1,128,1), sep="_")
total_acc_z_test <- read.table("test/Inertial Signals/total_acc_z_test.txt", header = FALSE, col.names =total_acc_z_labels)

# finnally :  creating the testing set
#merging the three data frames
test <- cbind(subjects,y_test, x_test,
              body_acc_x_test,
              body_acc_y_test,
              body_acc_z_test,
              body_gyro_x_test,
              body_gyro_y_test,
              body_gyro_z_test,
              total_acc_x_test,
              total_acc_y_test,
              total_acc_z_test)

# at last we merge the test and train sets

test_train <- rbind(train,test)



#we write the data to a csv file
write.csv(test_train,file="train_test_meged.csv")


#extracting mean and std
mean_std <- test_train[grep("*mean*|*std*",names(test_train),ignore.case = TRUE)]

#exporting to csv
write.csv(mean_std, file="mean_std_measurments.csv")

# 5 data set with the average of each measurment for each subject and activity

avg_sub_act <- aggregate(.~subject_id+activity, test_train, mean)

avg_sub_act
# exporting it to a text file

#write.table(avg_sub_act,file="finalDataSet.txt",row.name = FALSE)