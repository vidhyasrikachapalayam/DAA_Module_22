# EX 4A DYNAMIC PROGRAMMING - 1
## DATE:
## AIM:
To find longest common subsequence using Dynamic Programming.

## Algorithm
1. 
2. 
3. 
4.  
5.   

## Program:
```
/*
Program to implement the longest common subsequence using Dynamic Programming

.
Developed by: Vidhyasri K
Register Number:  212222230170
*/
```
```
def lcs(x,y,m,n):
    if m==0 or n==0:
        return 0
    elif x[m-1]==y[n-1]:
        return 1+lcs(x,y,m-1,n-1)
    else:
        return max(lcs(x,y,m,n-1),lcs(x,y,m-1,n))
X = input()
Y = input()
print ("Length of LCS is :", lcs(X , Y, len(X), len(Y)) )
```


## Output:



## Result:
Thus the program was executed successfully for computing the length of longest common subsequence.
