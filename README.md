# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1.Import NumPy for matrix operation

2.Get the coefficient matrix and constant matrix.
 
3.Apply gaussian Elimination to solve the system of linear equation
 
4.Print the solution and end the program.  

## Program:
'''Program to solve a matrix using Gaussian elimination without partial pivoting.
Developed by: T A Keerthana
RegisterNumber: 26009041
'''
import os
os.environ["OPENBLAS_NUM_THREADS"]="1"
import numpy as np
import sys

n = int(input())
a = np.zeros((n,n+1))
x = np.zeros(n)
for i in range(n):

    for j in range(n+1):
    
        a[i][j]=float(input())
        
for i in range(n):

    if a[i][i]==0.0:
    
        sys.exit('Divide by zero detected!')
        
    for j in range(i+1,n):
    
        ratio=a[j][i]/a[i][i]
        
        for k in range(n+1):
        
            a[j][k] = a[j][k] - ratio*a[i][k]

x[n-1] = a[n-1][n]/a[n-1][n-1]

for i in range(n-2,-1,-1):
    x[i] = a[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-a[i][j]*x[j]
    x[i] =x[i]/a[i][i]

for i in range(n):
    print('X%d = %0.2f' %(i,x[i]),end=' ')
        
        
    


    
        
        
        
    

## Output:
<img width="1087" height="880" alt="image" src="https://github.com/user-attachments/assets/bf533741-d989-4e1a-842e-78028968698f" />
<img width="1163" height="631" alt="image" src="https://github.com/user-attachments/assets/945e6cf9-6f84-484e-81fa-aecaa8020db9" />




## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

