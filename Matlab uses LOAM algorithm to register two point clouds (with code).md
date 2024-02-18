#  Function overview 

##  1. Algorithm overview 

   Register two point clouds using the LOAM algorithm 

##  2. Main functions 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574512133
  ```  
   Register movingPoints with fixedPoints using the LiDAR Mileage and Mapping (LOAM) algorithm. This function returns the rigid transform tform between movingPoints and fixedPoints. gridStep specifies the size of the 3D box used to downsample points detected in the input point cloud. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574512133
  ```  
 Matches LOAM points in movingPoints and LOAM points on fixedPoints, and returns the rigid transformation between them. Using this feature to match LOAM points is faster and more accurate than using it to match point clouds. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574512133
  ```  
 Returns the root mean square error rmse of the Euclidean distance between corresponding points. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574512133
  ```  
 Specifies options using one or more name-value arguments and any combination of arguments from previous syntax. For example, MatchingMethod = 'one-to-one' sets the matching method algorithm to'one-to-one '. Enter parameters 

 Name-value corresponding parameter 

 output parameter 

##  3. References 

>  [1] Zhang, Ji, and Sanjiv Singh. “LOAM: Lidar Odometry and Mapping in Real-Time.” In Robotics: Science and Systems X. Robotics: Science and Systems Foundation, 2014. https://doi.org/10.15607/RSS.2014.X.007. 

#  Code implementation 

 Align Two Point Clouds Using LOAM Registration Algorithm 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574512133
  ```  
 Align Two Point Clouds Using LOAM Points 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574512133
  ```  
#  III. Display of results 

 ![avatar]( 15fecd17ff7f44e6a567a4339571cc17.png) 

 Align Two Point Clouds Using LOAM Registration Algorithm  Align Two Point Clouds Using LOAM Points  

#  IV. Reference link 

 Matlab point cloud toolbox - pcregisterloam 

