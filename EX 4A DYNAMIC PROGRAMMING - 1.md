# EX 4A DYNAMIC PROGRAMMING - 1
## DATE:
## AIM:
To find longest common subsequence using Dynamic Programming.

## Algorithm
1. Start
2. Input strings X and Y
3. Define a function lcs(x, y, m, n):

     a. If m == 0 or n == 0:

     → Return 0

      b. If x[m-1] == y[n-1]:

      → Return 1 + lcs(x, y, m-1, n-1)

      c. Else:

      → Return max(lcs(x, y, m, n-1), lcs(x, y, m-1, n))
4.  Call the function lcs(X, Y, len(X), len(Y))
5. Print the result  

## Program:
```
Program to implement the longest common subsequence using Dynamic Programming
Developed by: Vidhyasri K
Register Number:  212222230170

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
![image](https://github.com/user-attachments/assets/bad37f59-aa0b-4f54-b957-aeed42fe71e4)

## Result:
Thus the program was executed successfully for computing the length of longest common subsequence.
