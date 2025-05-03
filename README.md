# K-Means-Clustering


  
 
 
 


 
K-Means Clustering 
 
 
 
 
 
 	 



 
There are two main types of machine learning methods. Supervised learning techniques require labeled training data. Unsupervised learning techniques do not need label instances. Instead, they try to find patterns within the data itself.  
  
  
  
  
Clustering  
Clustering is a popular unsupervised learning technique which helps find patterns in the underlying data. Clustering does not use any Y variables or labels on the data. It looks at the data structure itself. Let's first understand how clustering works and how we can use it with any kind of data.  
 The important principle behind clustering is that anything can be represented by a set of numbers. Whether it's an object, a person, a document, or a webpage, all of these can be represented in some numeric form. Let's consider a person. A person is of a certain age that can be represented on a number line.  
  
  
  
  
 A person may be of a certain height. All you need to do then is to represent this information in two dimensions. The person is a point on this plane.  
  
  
  
  
Let's say you were to add a third dimension. A person has a certain weight. Now this individual is represented using three distinct pieces of data.   
  
    
Now, assume you have a whole bunch of other information about this person, you could then use an N dimensional Hypercube to represent the set of N numbers. The basic principle is that all the information about a particular person can be represented in numeric form.  Now let's take the example of Facebook users. Facebook users have certain characteristics. Different users have different characteristics. Hypothetically, you could have a set of Facebook users where each user is a point in an N dimensional Hypercube.   
  
Clustering involves finding groups of people within this data who have the same characteristics. It could be that they like the same music, they went to the same high school, anything. Clustering results in the formation of groups within the data where people within the same group are similar. People who are in different groups are different.   
  
  
  
Let's say you were to change the features on the basis of which you performed clustering. You could end up with a completely different set of groups. One of these groups could be parents with children under five. Another group could be parents of teenagers.  
  
  
  
 If you think about the Facebook example, clustering of users is important because then you can target specific ads to specific groups. So, how well did your algorithm cluster the underlying data? This can be measured by considering the distance between individual points in a cluster. Smaller this distance, better the clustering. The distance between users in a cluster is a measure of how similar the users are and the goal of clustering is to maximize intra-cluster similarity.  
In addition, we also want our clustering algorithm to ensure that the distance between users who are in different clusters is as large as possible. We want to minimize inter-cluster similarity. A good clustering algorithm will try and achieve both of these objectives to the best of its ability, maximize intra-cluster similarity, and minimize inter-cluster similarity.  
  
  
  
  
K-Mean Clustering  
  
One of the most popular machine learning algorithms to perform clustering which allows us to maximize inter-cluster similarity and minimize intra-cluster similarity is the K-means clustering algorithm.   
Let's say we have a number of points in two-dimensional space. This can be extended to N dimensional space. We'll work with two dimensions because that's simpler to visualize. We start off by initializing K centroids or the K-means of the clusters.   
  
    
In K-means clustering you have to specify this value of K up front, how many clusters you want your data to be divided into. Lets assume 4 different centroids in our example.  
  
  
Once you have K cluster centers assign each point to a particular cluster. In order to do this, we calculate the distance between every point and every cluster center. A point is assigned to that cluster whose cluster center it is the closest to.  
  
  
    
Once you've assigned all the points, you'll see a cluster set up like this. At this point in time, use the existing points in each cluster to recalculate the mean for each cluster. Once the cluster centers have been recalculated, you'll find that certain points will move to another cluster.  
  
 We recalculate the distance from all cluster centers and reassign the points. This process of recalculating the means of each cluster and then reassigning the points once the new means have been calculated continues till the points reach their final position. When the cluster centers and the corresponding points don't move anymore, that's when the algorithm has converged. After convergence, you can think of every cluster being represented by a single point and this point is the reference vector. This reference vector is the center of the cluster and because it is calculated as an average of all points that belong to a cluster it's called the centroid of the cluster.  
  
  
 
  
  
  
Dataset:  
  
Dataset we are using here is the Mall Customers data (csv provided).It’s unlabeled data that contains the details of customers in a mall (features like genre, age, annual income (k$), and spending score ). Our aim is to cluster the customers based on the relevant features; gender, age, annual income and spending score.  
Task 1  
To do:  
1.Load the data  
  
 
 
  
2.Apply some pre-processing (remove unwanted columns, convert categorical data to numerical) 
 
 
 
 
 
 
 
3.Now it’s time to implement the K mean clustering algorithm. Define s function Kmeans that takes data and value of k as input and groups the data into k clusters. You can start with k = 3 and then evaluate your code for different values of K.  
    
 Task 2:

Dataset: 
You will use the "Online Retail" dataset, which is publicly available on the UCI Machine Learning 
Repository. The dataset contains transactional data of a UK-based online retail company from 2010 to 2011. It includes features such as customer ID, product description, quantity purchased, and price. I will also upload the dataset. 
 
•Load the dataset: Load the "Online Retail" dataset into your programming environment.  
•Explore the dataset: Perform an initial exploration of the dataset to understand its structure, feature types, and potential issues. Identify the relevant features that can be used for customer segmentation using K-means clustering. 
•Preprocess the data: Preprocess the dataset to handle any missing values, remove irrelevant features, and transform the data into a suitable format for K-means clustering. You may need to consider data cleaning, feature scaling, or encoding categorical variables if necessary. 
•Implement K-means clustering: Implement the K-means clustering algorithm using a suitable programming language or library. You can use libraries such as scikit-learn, TensorFlow, or Keras that provide K-means clustering functionality. 
•Determine the optimal number of clusters: Utilize an appropriate method to determine the optimal number of clusters for the given dataset sing elbow method. 
•Cluster the data: Apply the K-means clustering algorithm to the preprocessed dataset, using the optimal number of clusters determined in the previous step. Assign each customer to one of the identified clusters. 
•Analyze the clusters: Perform an in-depth analysis of the obtained clusters. Interpret the results by analyzing the characteristics and behavior of customers in each cluster. Provide insights on how the retail company can utilize this information to improve their marketing strategies or customer targeting. 
•Visualize the results: Visualize the clusters and their characteristics using appropriate plots or visualizations. Use techniques like scatter plots, histograms, or bar charts to present the findings in a clear and understandable manner. 
 
