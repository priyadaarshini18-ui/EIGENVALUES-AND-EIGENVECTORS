# EIGENVALUES-AND-EIGENVECTORS
## Aim:
To write a python program to find the Eigenvalues and Eigen Vectors
## Equipment’s required:
1. 	Hardware – PCs
2. 	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Step1 : Import required libraries os and numpy. Set OPENBLAS_NUM_THREADS to "1" to avoid threading warnings.
### Step 2: Create matrix `A = np.array([[4, 2], [2, 4]])
### Step 3: Using the np.linalg.eig(),  we get two results (first is eigenvalue and second is eigenvector) of the given matrix.
### Step 4: Sort eigenvalues descending, rearrange eigenvectors, print result.

## Program:
```
#Program to find the eigen values and eigen vectors.
#Developed by: v.priyadaarshini
#RegisterNumber:212225040317
import os
os.environ["OPENBLAS_NUM_THREADS"] = "1"
import numpy as np

A = np.array([[4, 2],
              [2, 4]])

eigenvalues, eigenvectors = np.linalg.eig(A)

idx = eigenvalues.argsort()[::-1]
eigenvalues = eigenvalues[idx]
eigenvectors = eigenvectors[:, idx]

print(f"Eigen values are {eigenvalues} and Eigen Vectors are {eigenvectors}")
```
## Output:
![alt text](<Screenshot 2026-05-19 212050.png>)
## Result:
Thus the Eigenvalue and Eigenvector is successfully solved using python program
