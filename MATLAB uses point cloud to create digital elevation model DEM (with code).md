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

