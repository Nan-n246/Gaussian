# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. import numpy and sys to use the built-in-function for calculation.
2. Get the size of the matrix(order) from the user and initialize an empty matrix and vector
3. use for loop to get elements of the matrix and vector from the user
4. using another for loop to take each element in the matrix and solve inrow echelon form
   

## Program:
```
/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: NANDHINI S
RegisterNumber:24013591
import numpy as np
import sys
n=int(input())
a=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
      a[i][j]=float(input())
for i in range(n):
    if a[i][i] ==0.0:
      sys.exit('Divide by zero detected!')    
    for j in range(i+1,n):
      ratio = a[j][i]/a[i][i]
      for k in range(n+1):
          a[j][k]= a[j][k]-ratio*a[i][k]
x[n-1]=a[n-1][n]/a[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i]=a[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-a[i][j]*x[j]
    x[i]=x[i]/a[i][i]
for i in range(n):
    print('X%d = %0.2f '%(i,x[i]),end='' )
     
*/
```

## Output:
![alt text](<Screenshot 2024-12-11 141955.png>)


## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

