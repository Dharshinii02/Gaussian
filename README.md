# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. Import numpy and define the matrix with coefficients and constants
2. Convert the matrix to an upper triangular matrix
3. Solve for variables starting from the last row and print
4. End the program

## Program:
```

Developed by: dharshini j
RegisterNumber: 24900678
import numpy as np
import sys
n=int(input())
a=np.zeros((n,n+1))
x=np.zeros(n)

for i in range(n):
   for j in range(n+1):
      a[i][j]=float(input())

for i in range(n):
   if a[i][i]==0.0:
     sys.exit('Divide by zero detected!')
   for j in range(i+1,n):
      ratio=a[j][i]/a[i][i]
      for k in range(n+1):
         a[j][k]=a[j][k]-ratio*a[i][k]
x[n-1]=a[n-1][n]/a[n-1][n-1]
for i in range(n-2,-1,-1):
   x[i]=a[i][n]
   for j in range(i+1,n):
      x[i]=x[i]-a[i][j]*x[j]
   x[i]=x[i]/a[i][i]
for i in range(n):
   print('X%d = %0.2f '%(i,x[i]),end='')

```

## Output:

![Screenshot 2024-11-27 133910](https://github.com/user-attachments/assets/cea34e7f-df57-4e6f-be72-01d4385df259)

## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

