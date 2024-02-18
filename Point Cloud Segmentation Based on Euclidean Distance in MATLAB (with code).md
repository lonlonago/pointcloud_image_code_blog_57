#  Function overview 

##  1. Implementation process 

 ![avatar]( 20210516100352615.png) 

   Euclidean clustering is a clustering algorithm based on the Euclidean distance metric. The nearest neighbor query algorithm based on KD-Tree is an important preprocessing method to accelerate the Euclidean clustering algorithm. The process is as follows:  

   For Euclidean clustering, the distance criterion is the Euclidean distance mentioned above. For a point P in space, the k points closest to the p point are found through the KD-Tree nearest neighbor search algorithm, and those points whose distance is less than the set threshold are clustered into the set Q. If the number of elements in Q does not increase, the whole clustering process ends; otherwise, the points other than the p point must be selected in the set Q, and the above process is repeated until the number of elements in Q does not increase. 

##  2. Main functions 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574521876
  ```  
   The point cloud is divided into clusters with the minimum Euclidean distance as the minimum distance between different clustering points. pcsegdist assigns an integer cluster label to each point in the point cloud and returns the labels of all points. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574521876
  ```  
 Returns the number of clusters, along with the labels of all points. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574521876
  ```  
 Specify the minimum and maximum number of points in each cluster. 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574521876
  ```  
#  III. Display of results 

##  1. Segmentation results 

 ![avatar]( 684e89cbd3bf456689f55e920c6b8d90.png) 

##  2. Save the results 

 ![avatar]( 3ac8bcbea0604e7c8f73bcb000105af4.png) 

#  IV. Reference link 

 matlab点云工具箱——Segment point cloud into clusters based on Euclidean distance 

