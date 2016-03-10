UECM3033 Assignment #2 Report
========================================================

- Prepared by: **ANG HUANG YING **
- Tutorial Group: T2

--------------------------------------------------------

## Task 1 --  $LU$ Factorization or SOR method

The reports, codes and supporting documents are to be uploaded to Github at: 
https://github.com/anghuangying/UECM3033_assign2.git

Explain your selection criteria here.
The condition is set to be np.count_nonzero(A) > 1/2*len(A). Sparse matrix is a matrix where most of the elements are zeros and allows special techniques to take advantage to reduce both the storage and work required in solving a linear system. Therefore, LU method will be chosen if the non-zero is greater than half of the length of matrix A. For iterative methods, SOR method  are adequate to use the sparse matrix.

Explain how you implement your `task1.py` here.
In task 1 , implement function of lu, sor and solve are created. For LU method, two matrix will be created with is the lower triangular matrix and upper triangular matrix whereby A=LU, thus Ax=LUx=b and therefore it will be define into Ly=b and Ux= y. The x matrix will be calculated after getting the y matrix. For the SOR method, assume the omega as 1.03 which is within the range of 1 < omega < 2 that will converge for any initial vector if A matrix is symmetric and positive definite. If omega is greater than 2 , SOR method will diverge. If 0 < omega<1, SOR method converges but the convergence rate is slower than the Gauss-Seidal method. For the iteration limit needed to be set so that it will not loop until infinity time. In this task, the iteration limit is set to be 10. Begin the iteration by assuming the first x as zero vector. Then substitute each x we found to calculate the new x and iterate until the iteration limit. In order to find the precise answer, assign sol equal to np.linalg.solve(A,b) else the answer will not be accurate.


---------------------------------------------------------

## Task 2 -- SVD method and image compression

Put here your picture file (flowers.jpg)
![flowers.jpg](flowers.jpg)


How many non zero element in $\Sigma$?
All the elements (R,G,B) in $\Sigma$ are non zero. 

Put here your lower and better resolution pictures. Explain how you generate
these pictures from `task2.py`.

What is a sparse matrix?


-----------------------------------

<sup>last modified: change your date here</sup>
