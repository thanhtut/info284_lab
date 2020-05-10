##$ Lab 14: Agglomerative Clustering from stractch ##
Before we start, this week lab actually what was planned for the assignment 3. However, we have to pace the course slower. So, now this is a lab for this week. It is more than a lab but you dont have to finish it in a week you can try it at our own pace and ask the TAs and me for help if you have any problems with it.

### Agglomerative clustering with single linkage ###
Agglomerative clustering with 'single' linkage. In this exercise, we are going to implement agglomerative hierarchical clustering with using 'single' method to measure the distance between clusters. To learn the agglomerative clustering with 'single' linkage study the following resources.
* Lecture "Supervised Learnign II"
* Introduction to machine learning with Python p 184
* The API and description of sklearn [AgglomerativeClustering](https://scikit-learn.org/stable/modules/generated/sklearn.cluster.AgglomerativeClustering.html)
* [Video Tutorial](https://www.youtube.com/watch?v=RdT7bhm1M3E&t=401s) on Agglomerative Clustering
* Another [Medium post](https://towardsdatascience.com/understanding-the-concept-of-hierarchical-clustering-technique-c6e8243758ec) for agglomerative clustering

### Task ###
Implement agglomerative clustering with single linkage criteria from scratch and use euclidean distance. Test it on the sklearn iris dataset (pick only two feature) and compare it with the output of sklearn.cluster.AgglomerativeClustering class. 

Requirements
* The class should have a constructor which takes the number of clusters as an argument (n_clusters)
* The class should have fit() method which takes an array of two dimensional dataponts. e.g. np.array([5.1,3.5], [4.3,3.0],[5.9,3.0],[6.5,3.0]) 
* The fit method should computer the labels of the clusters starting from 0 using agglomerative clustering with single linkage method. e.g. [1,0,1,1]. Then the computed labels should be stored in labels_ attribute of the object of your class. 

