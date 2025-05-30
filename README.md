# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
STEP1:Input the Number of Equations (n)
Read the size of the system (number of equations and variables).

STEP2:Initialize Matrices
Create an augmented matrix a[n][n+1] and a solution array x[n], initialized to zero.

STEP3:Read Coefficients and Constants
Input the coefficients of the variables and the constant terms into the augmented matrix.

STEP4:Forward Elimination Begins
Loop through each row i to convert the matrix to upper triangular form.

STEP5:Check for Division by Zero
Before performing row operations, check if the diagonal element a[i][i] is zero. If it is, exit the program with an error.

STEP6:Apply Row Operations
For each row j below row i, compute the ratio of a[j][i] / a[i][i] and subtract ratio * row i from row j.

STEP7:Form Upper Triangular Matrix
Continue this process until the matrix is in upper triangular form (all zeros below the main diagonal).

STEP8:Start Back Substitution
Begin solving for variables starting from the last equation (x[n-1]).

STEP9:Compute Remaining Variables
Use previously computed values to solve the upper equations using back substitution.

STEP10:Display the Solution
Print each variable x[i] rounded to two decimal places.



## Program:
```
/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by:Dhineshkumar.L 
RegisterNumber:212224230066
import numpy as np
n=int(input())
a=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        a[i][j]=float(input())
for i in range(n):
    if a[i][i]==0.0:
        sys.exit('Divide by zero detected')
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
for i in range (n):
    print('X%d = %0.2f' %(i,x[i]),end=' ')


*/
```

## Output:
![alt text](<Screenshot 2025-04-24 183148.png>)



## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

