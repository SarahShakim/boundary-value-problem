# boundary-value-problem

## Implementing a solution that can solve a boundary value problem by creating a matrix of values that are points approximated for the function. The forcing function is on the right-hand side to represent the time-dependent function. 

Parameters

c = Vector of values that represent the coefficients of the ODE

x_int = Vector of values representing the boundaries of x

u_int = Vector of values representing the boundaries of u

g = Forcing function

n = Scalar value representing the number of values we want returned

**To solve the boundary value problem:**
1. Define an equation for the sub diagonal that is going to be used
2. Define an equation for the center diagonal that is going to be used
3. Define an equation for the super diagonal that is going to be used
4. Define the h value based off the boundaries of x
5. Define an array of x-values and took out the first and last value
6. Define the error term
7. Initialize a (n-2)x(n-2) vector that is filled with zeros
8. Take the transpose of b to allow it to be compatible with the other matrix
9. Create a vector of the d-values repeated the number of times it will appear on the diagonal of the matrix
10. Placed the respective d-values in their diagonals
11. Add the diagonal values to the intialized zeros matrix
12. Plot the points of the approximation 

**Example: Plotting the solution where the forcing function is a vector of zeros**

Calling **bvp( [1 3 2], @g1, [0,1], [4,5], 69)** where @g1 is the forcing function 

![image](https://user-images.githubusercontent.com/58648072/130007477-b36a64ad-1048-4811-bfea-687ec8b81d5b.png)

**Example: Solving an ODE where: c1 = 1, c2 = -3, c3 = 2, a = 0, b = 1, u_a = 1, u_b = 2**

![image](https://user-images.githubusercontent.com/58648072/130007718-d26680e0-86f6-46e1-b8b6-dbf0f75dd6c5.png)

