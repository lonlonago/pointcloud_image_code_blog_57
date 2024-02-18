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



--------------------------------------------------------------------------------

#  I. DEM 

##  1. Digital Elevation Model 

    Digital Elevation Model (Digital Elevation Model), referred to as DEM, is a digital simulation of ground terrain (that is, the digital expression of terrain surface morphology) through limited terrain elevation data. It is an entity ground model that represents ground elevation in the form of a set of ordered numerical arrays. It is a branch of Digital Terrain Model (DTM), from which various other terrain characteristic values can be derived. Generally speaking, DTM is a spatial distribution that describes a variety of geomorphological factors including elevation, such as slope, aspect, slope change rate, etc., including linear and nonlinear combinations. Among them, DEM is a zero-order simple single-item digital geomorphological model. Other geomorphological characteristics such as slope, aspect, and slope change rate can be derived on the basis of DEM. One article to understand DEM DSM DOM TDOM tilt photography 3D modeling, laser point cloud... 

##  2. Main functions 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574558570
  ```  
    Creates and returns a digital elevation model (DEM) elevModel for the input point cloud. The output matrix contains generalized elevation information for the input point cloud. This function creates a digital elevation model (DEM) for the point cloud data using a local binning algorithm. The algorithm assumes that the elevation of the point is along the z-axis. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574558570
  ```  
    Specifies the size of the grid element. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574558570
  ```  
    Using any combination of the input parameters of the syntax, returns the sum limit of the DEM. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574558570
  ```  
    Specify options using one or more name-value arguments. For example, the'CornerFillMethod, min 'specifies that the function computes the generalized elevation value of the grid angle in the DEM as the minimum elevation value within the default search radius for each grid angle. 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574558570
  ```  
#  III. Display of results 

##  1. Primitive point cloud 

 ![avatar]( 0e5283ff01be47459dce4c64000471db.png) 

##  2. The ground point 

 ![avatar]( 3f4d8e2825654a548f88535a98c5e7ef.png) 

##  3、DTM 

 Here DTM is DEM, see DTM-Baidu Encyclopedia for details. 

 ![avatar]( 1a3ad584f9b04e89a611528fe19efd70.png) 

#  IV. Parameter analysis 

##  input parameter 

##  Name value corresponding parameter 

>  'Min '- the minimum height of all points within the search radius'max' - the maximum height of all points within the search radius'mean '- the average height of all points within the search radius'idw' - inverse distance weighted (IDW), the average elevation of all points within the search radius 

##  output parameter 

#  V. Reference links 

 Matlab point cloud toolbox - pc2dem 

#  Warning!!! 

   The pc2dem function is a new function in matlab 2021b and above, so why do some bosses make mistakes?? Why ask??????  



--------------------------------------------------------------------------------

#  I. DEM 

##  1. Digital ground model 

    A digital ground model is a database that represents the spatial distribution of ground features. Generally, a series of ground point coordinates (x, y, z) and surface attributes (target categories, features, etc.) are used to quilt into a data array to form a digital ground model. Sometimes the terrain feature points referred to only refer to the elevation of the ground points, and this digital terrain description is called a digital elevation model (DEM). DSM represents the most realistic expression of ground fluctuations and can be widely used in all walks of life. For example, in forest areas, it can be used to detect the growth of forests; in urban areas, DSM can be used to check the development of cities; in particular, the well-known cruise missile requires not only a digital ground model, but also a digital surface model, so that it is possible to make cruise missiles fly at low altitudes, making mountains and forests. 

##  2. Main functions 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574583465
  ```  
    Creates and returns a digital elevation model (DEM) elevModel for the input point cloud. The output matrix contains generalized elevation information for the input point cloud. This function creates a digital elevation model (DEM) for the point cloud data using a local binning algorithm. The algorithm assumes that the elevation of the point is along the z-axis. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574583465
  ```  
    Specifies the size of the grid element. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574583465
  ```  
    Using any combination of the input parameters of the syntax, returns the sum limit of the DEM. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574583465
  ```  
    Specify options using one or more name-value arguments. For example, the'CornerFillMethod, min 'specifies that the function computes the generalized elevation value of the grid angle in the DEM as the minimum elevation value within the default search radius for each grid angle. 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574583465
  ```  
#  III. Display of results 

##  1. Primitive point cloud 

 ![avatar]( a432fbd7e35944faac8201dbbb8ffae1.png) 

##  2、DSM 

 ![avatar]( 609dc4dd7d6342fea5125774d2d90079.png) 

#  IV. Reference link 

 Matlab point cloud toolbox - pc2dem 



--------------------------------------------------------------------------------

#  Function overview 

   Write 3D surface mesh to STL or PLY file 

##  1. Main function 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574528448
  ```  
   Writes the curved mesh to an STL or PLY file with the specified filename. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574528448
  ```  
 Also specify the encoding type as "ascii" or "binary". 

##  2. Input and output parameters 

##  3. Insufficient 

 These properties cannot be read from an STL file: 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574528448
  ```  
#  III. Display of results 

 ![avatar]( 471b11afb4fa4c9ebc8bdd05a6d8902c.png) 

#  Fourth, a warning!!! 

   Copy and paste the code to run directly, and do not read other content of the blog. If you report an error, you will directly open "Why did I report an error, what kind of garbage code is this"??? readSurfaceMesh is a new function in matlab2022b and above, so why do some bosses make mistakes?? Why ask?????  



--------------------------------------------------------------------------------

#  First, Moore-Penrose pseudo-inverse 

    A Moore-Penrose pseudo-inverse is a matrix that can be used as a partial substitute for an inverse matrix in the absence of an inverse matrix. This matrix is often used to solve systems of linear equations that have no unique solution or many solutions. For any matrix, a pseudo-inverse exists, is unique, and has the same dimensions as. If it is a square matrix and not singular, it is only a relatively expensive way to calculate. However, if it is not a square matrix, or if it is a square matrix and singular, it does not exist. In these cases, some (but not all) properties of: 

 1. 2. 3. (AB Hermitian) 4. (BA Hermitian) 

 The pseudo-inverse calculation is based on svd (A). This calculation treats singular values less than tol as zero. 

     A pseudo-inverse formed by singular value decomposition. Singular values less than diagonally are treated as zero, and the representation of, becomes:  

 Therefore, the false inverse is equal to: 

##  1. Main function 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574589499
  ```  
    Returns the Moore-Penrose pseudo-inverse of a matrix. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574589499
  ```  
     Specifies the value of the tolerance. Treats any singular value less than the tolerance as zero. 

##  2. Input and output parameters 

#  Code example 

##  Using Pseudo-Inverse to Solve Linear Equations 

    Compare the solutions of a system of linear equations obtained by backslash () and pinv. If the rectangular coefficient matrix A is of low rank, the least squares problem that minimizes norm (A * x-b) will have an infinite number of solutions. X1 = A\ b and x2 = pinv (A) * b return two solutions. These two solutions have the following characteristics: x1 has only rank (A) non-zero components, and norm (x2) is the norm less than any other solution. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574589499
  ```  
 Calculation result 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574589499
  ```  
 Create a vector for the right side of the system of equations. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574589499
  ```  
 Calculation result 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574589499
  ```  
    The number 260 chosen for the right is the 8 × 8 magic sum of A. If A is still an 8 × 8 matrix, then x has a solution that is a vector of 1. If there are only six columns, the equation is still consistent, so there is still a solution, but the solution is not all composed of 1. Since the matrix is of low rank, there are an infinite number of solutions. Use a backslash and pinv to find two solutions. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574589499
  ```  
 Calculation result 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574589499
  ```  
  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574589499
  ```  
 Calculation result 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574589499
  ```  
    Both solutions are accurate in the sense that norm (Ax1-b) and norm (Ax2-b) have only rounding errors. The special thing about solution x1 is that it has only three non-zero elements. The special thing about solution x2 is that norm (x2) is less than the corresponding value of any other solution, including norm (x1). 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574589499
  ```  
 Calculation result 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574589499
  ```  
  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574589499
  ```  
 Calculation result 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574589499
  ```  


--------------------------------------------------------------------------------

#  First, the angle of rotation 

##  1. Main function 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574577931
  ```  
    Converts the angular units of each element in R from radians to degrees. 

##  2. Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574577931
  ```  
#  Second, the angle of radian rotation 

##  1. Main function 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574577931
  ```  
    For each element of D, R = deg2rad (D) converts the unit of angle from degrees to radians. 

##  2. Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574577931
  ```  
#  III. Trigonometric functions 

 In MATLAB, sind, cosd, and tand are expressed in angles, while sin, cos, and tan functions are expressed in radians. 

#  IV. Relevant links 

 [1] rad2deg [2] deg2rad 



--------------------------------------------------------------------------------

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



--------------------------------------------------------------------------------

#  First, the main function 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574583138
  ```  
   Returns a column vector of logical values that indicates whether a triangle in a 2D constrained Delaunay triangulation is within a bounded geometric domain. The element of TF is 1 (true) when the corresponding triangle in DT is within that domain, and 0 (false) otherwise. 

#  Code example 

 Triangle within the specified boundary, computes and plots the constrained two-dimensional Delaunay triangulation of the triangle within the specified boundary. 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574583138
  ```  
##  3. Display of results 

 ![avatar]( 139024e1b9a54bb699572667950a5036.png) 

    Constraints between vertices (V1, V3) have been followed, but the Delaunay rule is invalidated. In addition, the nearest neighbor relationship inherent in Delaunay triangulation is invalidated. This means that if the triangulation contains constraints, the nearestNeighbor search method provided by delaunayTriangulation cannot be supported. 



--------------------------------------------------------------------------------

#  First, the principle of the algorithm 

   The method is mainly used to roughly count the area occupied by airborne point clouds. The principle of the method is to divide the point cloud into a grid along the surface, and count the grid area of the points to approximately represent the area occupied by the point cloud. 

#  Code implementation 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957452034
  ```  
#  III. Display of results 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 202402030957452034
  ```  
 ![avatar]( f7042097b881433ebedd6033ad032482.png) 

#  IV. Test data 

 Link: https://pan.baidu.com/s/1qPJY2usVBWGkdaq8VNoDog extraction code: ftx5 



--------------------------------------------------------------------------------

#  一、KD-Tree 

##  1. K-nearest neighbor search 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574520963
  ```  
   Returns the index of the K nearest neighbors of the query point in the input point cloud. PtCloud can be an unorganized or organized point cloud. The K nearest neighbors of the query point are calculated using a search algorithm based on KD tree. 

##  2. Radius search 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574520963
  ```  
#  Code implementation 

##  1. K-nearest neighbor search 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574520963
  ```  
##  2. Radius search 

  ```python  
After clicking on the GitHub Sponsor button above, you will obtain access permissions to my private code repository ( https://github.com/slowlon/my_code_bar ) to view this blog code. By searching the code number of this blog, you can find the code you need, code number is: 2024020309574520963
  ```  
#  III. Display of results 

 ![avatar]( 20210605155729529.png) 

#  IV. Reference link 

 matlab点云工具箱——Find nearest neighbors of a point in point cloud matlab点云工具箱——Find neighbors within a radius of a point in the point cloud 



--------------------------------------------------------------------------------

