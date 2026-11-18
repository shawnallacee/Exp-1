# Experiment 1: Exploring NumPy and Pandas

## Aim

To understand the use of NumPy and Pandas for performing basic data
manipulation and analysis in Python.

## Algorithm

1.  Import the NumPy library for matrix and numerical operations.
2.  Define a two-dimensional square matrix `A` and a vector `b`.
3.  Compute the transpose of matrix `A` to interchange rows and columns.
4.  Calculate the inverse of matrix `A` using `np.linalg.inv(A)` (ensure
    `A` is non-singular).
5.  Solve the linear equation `A × x = b` using `np.linalg.solve(A, b)`.
6.  Perform eigen decomposition to find eigenvalues and eigenvectors
    using `np.linalg.eig(A)`.
7.  Display the results for the matrix, transpose, inverse, solution
    vector, and eigenvalues.
8.  End the program.

## Formulas / Theory

-   **Transpose:** `Aᵀ` --- interchange rows and columns.
-   **Inverse:** `A⁻¹ = adj(A) / |A|`, provided `det(A) ≠ 0`.
-   **Linear system:** `A × x = b  ⇒  x = A⁻¹b`.
-   **Eigen decomposition:** `A v = λ v`, where `λ` is an eigenvalue and
    `v` is an eigenvector.

## Coding
import numpy as np    
import pandas as pd    

\# Define a 2D square matrix A and a vector b    
print("--- 1. Matrix and Vector Definition ---")    
A = np.array([[4, 2],     
              [1, 3]], dtype=float)    
b = np.array([8, 5], dtype=float)    

print("Matrix A:")    
print(A)    
print("\nVector b:")    
print(b)    

\# Compute the transpose of matrix A    
print("\n--- 2. Matrix Transpose (A^T) ---")    
A_transpose = A.T    
print(A_transpose)    

\# Calculate the inverse of matrix A    
print("\n--- 3. Matrix Inverse (A^-1) ---")    
try:    
    A_inv = np.linalg.inv(A)    
    print(A_inv)    
except np.LinAlgError:    
    print("Matrix A is singular and cannot be inverted.")    

\# Solve the linear equation A * x = b    
print("\n--- 4. Solving Linear Equation (A * x = b) ---")    
x = np.linalg.solve(A, b)    
print("Solution vector x:", x)    

\# Perform eigen decomposition    
print("\n--- 5. Eigen Decomposition (A v = lambda v) ---")    
eigenvalues, eigenvectors = np.linalg.eig(A)    
print("Eigenvalues:", eigenvalues)            
print("\nEigenvectors:\n", eigenvectors)                

\# Bonus / Pandas Integration: Tabular Representation    
print("\n--- 6. Pandas Dataframe Summary ---")    
df_results = pd.DataFrame({    
    "Eigenvalue": eigenvalues,                
    "Eigenvector_Col1": eigenvectors[:, 0],    
    "Eigenvector_Col2": eigenvectors[:, 1]    
})                
print(df_results)        

## Output                                
<img width="458" height="650" alt="image" src="https://github.com/user-attachments/assets/4d8d9414-d0b1-4414-a7af-52f815f84916" />


## Result
Thus to understand the use of NumPy and Pandas for performing basic data
manipulation and analysis in Python successfully.
