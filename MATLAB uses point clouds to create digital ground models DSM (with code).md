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

