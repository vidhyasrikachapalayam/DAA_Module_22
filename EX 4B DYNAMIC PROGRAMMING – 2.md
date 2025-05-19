# EX 4B DYNAMIC PROGRAMMING – 2
## DATE: 05/04/25

## AIM:
To find the longest string (or strings) that is a substring (or are substrings) of two strings..

## Algorithm

1. Input two strings X and Y of lengths m and n.

2. Create a 2D matrix lookup of size (m+1) × (n+1) initialized to 0.

3. Initialize maxLength = 0 and endingIndex = m.

4. For each i from 1 to m:

5. For each j from 1 to n:

6. If X[i-1] == Y[j-1]:

7. Set lookup[i][j] = lookup[i-1][j-1] + 1

8. If lookup[i][j] > maxLength:

9. Update maxLength and endingIndex

10. The longest common substring is from : X[endingIndex - maxLength : endingIndex].

11. Return the longest common substring.
    
## Program:

Program to implement the longest common substring problem

Developed by: Vidhyasri k

Register Number: 212222230170

```
def LCS(X, Y, m, n):
    maxLength = 0
    endingIndex = m
    lookup = [[0 for x in range(n + 1)] for y in range(m + 1)]
    for i in range(1, m + 1):
        for j in range(1, n + 1):
            if X[i - 1] == Y[j - 1]:
                lookup[i][j] = lookup[i - 1][j - 1] + 1
                if lookup[i][j] > maxLength:
                    maxLength = lookup[i][j]
                    endingIndex = i
    return X[endingIndex - maxLength: endingIndex]

X = input()
Y = input()
m = len(X)
n = len(Y)
print('The longest common substring is', LCS(X, Y, m, n))       
```

## Output:

![image](https://github.com/user-attachments/assets/03fdab8b-96e1-418b-bf32-5e3322e0657c)


## Result:
Thus the program was executed successfully for finding the longest common substring .
