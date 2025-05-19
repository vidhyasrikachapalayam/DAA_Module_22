# EX 4A DYNAMIC PROGRAMMING - 1

## DATE: 01/04/25

## AIM:
To find longest common subsequence using Dynamic Programming.


## Algorithm

1. Input two strings str1 and str2.

2. Let m = length of str1, n = length of str2.

3. Create a 2D matrix matrix of size (m+1) x (n+1) initialized to 0.

4. For each i from 1 to m:

5. For each j from 1 to n:

6. If str1[i-1] == str2[j-1]:
   
   matrix[i][j] = 1 + matrix[i-1][j-1]
   
7. Else:

   matrix[i][j] = max(matrix[i-1][j], matrix[i][j-1])

8. Return matrix[m][n] as the length of the LCS.


## Program:

Program to implement the longest common subsequence using Dynamic Programming

Developed by: Vidhyasri k

Register Number: 212222230170

```
def lcs(str1 , str2):
    m = len(str1)
    n = len(str2)
    matrix = [[0]*(n+1) for i in range(m+1)] 
    for i in range(m+1):
        for j in range(n+1):
            if i==0 or j==0:
                matrix[i][j] = 0
            elif str1[i-1] == str2[j-1]:
                matrix[i][j] = 1 + matrix[i-1][j-1]
            else:
                matrix[i][j] = max(matrix[i-1][j] , matrix[i][j-1])
    return matrix[-1][-1]
str1 = input()
str2 = input()
lcs_length = lcs(str1, str2)
print("Length of LCS is : {}".format(lcs_length))
```

## Output:

![image](https://github.com/user-attachments/assets/5ecd5eed-88b5-497a-9d5f-e0f1e2763a0a)


## Result:
Thus the program was executed successfully for computing the length of longest common subsequence.
