# boundary-value-problem

## Implementing a solution that can solve a boundary value problem by creating a matrix of values that are points approximated for the function. The forcing function is on the right-hand side to represent the time-dependent function. 

Parameters

c = Vector of values that represent the coefficients of the ODE
x_int = Vector of values representing the boundaries of x
u_int = Vector of values representing the boundaries of u
g = Forcing function
n = Scalar value representing the number of values we want returned

To solve the boundary value problem:
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
