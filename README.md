# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1.First,we want to import numpy,then import sys,assume a variable.
2.For gaussian elimination method, we want to make 2nd and 3rd column zero.
3.For that we want to make a range accorting to our program output.
4.Then print the program with correct form then the output will display. 

## Program:
```
/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: v.kayalvizhi
RegisterNumber:212225040182
import os
os.environ["OPENBLAS_NUM_THREADS"]="1"
import numpy as np
def solve_gaussian(data):
    n=int(data[0])
    A=np.array(data[1:],dtype=float).reshape(n,n+1)
    for i in range(n):
        for j in range(i+1,n):
            factor=A[j,i]/A[i,i]
            A[j]-=factor*A[i]
    x=np.zeros(n)
    for i in range(n-1,-1,-1):
        x[i]=(A[i,-1]-np.dot(A[i,i+1:n],x[i+1:n]))/A[i,i]
    return x
data=[]
for i in range(13):
    data.append(input())
result=solve_gaussian(data)
print("".join([f"X{i} = {val:.2f} "for i,val in enumerate(result)]))


*/
```

## Output:
<img width="1251" height="630" alt="Screenshot 2026-05-20 092156" src="https://github.com/user-attachments/assets/4a1bca31-61ba-4995-979b-aea810c8e9f9" />
<img width="915" height="425" alt="Screenshot 2026-05-20 092207" src="https://github.com/user-attachments/assets/37cd00bc-a8e4-44ad-8bcd-8af51dc0f39c" />




## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

