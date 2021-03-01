# Probably_Interesting_Data
EECS 768 -Project 1
M. Atif Siddiqui 

Datasets 
I used the following datasets form UCI-ML 
1) Iris Species
2) Pima Indians Diabetes Database 

Models 
1) For Iris Species dataset I have implemented the K-Means algorithm. 
2) For Diabetes dataset I have implemented the K-nearest Neighbors algorithm.

Dataset: Iris Species
        Data Analysis
            1) Loaded the dataset in a dataframe using pandas.
            2) Checked the data for null values. 
            3) created a new dataframe (cluster_data) to work on two columns(SepalLength, PetalLength) of the previous dataframe.
            4) Sorted the new dataframe(cluster_data) 
            5) Converted the dataframe(cluster_data) to an numpy array.
            6) I found out that the last row of our array contain the name of the columns.
            7) Created a new array(cluster_array) that excludes the last row of our previous array.

        K-Means Algorithm
          General Idea:
          1) Randomly assign centroids to start things up.
          2) Based on those centroids (and an observation’s distance from it), assign each observation to a cluster.
          3) Calculate the mean coordinates of each cluster; these are our new centroids.
          4) Reassign clusters based on new centroids.
          5) Keep repeating steps 3 and 4 until convergence.
          Functions:
          1) EuclideanDistance: To calculate the Euclidean Distance between two datapoints. 
                Input: takes in two observation points and the size of the dataset.
                Output: the Euclidean Distance
          2) assign_clusters: To calculate the distance between every observational point and every centroids and then assign these points to clusters based on                   closet centroids.
                Input: takes in the centroids and the cluster_array
                Output: a list of each datapoint's cluster lable.
          3) calc_centroids: To calculate new centroids based on mean of each cluster.
                Input: takes in the clusters and cluster_array
                Output: a list of new centroids.
          4) calc_centroids_variance: To calculate the variance of each cluster. This fuction filters cluster_df by cluster. 
                Input: takes in clusters and the cluster_array
                Output: return a list sum_squares
                
Dataset: Pima Indians Diabetes Database 
          Data Analysis
            1) Loaded the dataset in a dataframe using pandas.        
            2) Checked the data for null values.
            3) Splitted the data into two part test_data and train_data
           
           K- Nearest Neighbors Algorithms 
           Functions: 
           1) EuclideanDistance: To calculate the Euclidean Distance between two datapoints. 
                Input: takes in two observation points and the size of the dataset.
                Output: the Euclidean Distance
           2) functionToFindK: Helps in finding the K-value
                Input: takes in the square root of the number of records in training dataset
                output: returns an odd number that can be used as K
            3) KNN: main function for K-Nearest Neighbors 
                Input: takes in the training and test dataset 
                Output: Prints the value of K and its nearest neighbors. 
