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
