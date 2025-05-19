# EX 4C DYNAMIC PROGRAMMING – 3
## DATE: 08/04/25

## AIM:
Given a sequence, find the length of the longest palindromic subsequence in it.

## Algorithm

1. Input string seq of length n.

2. Set s2 = reverse of seq.

3. Initialize 2D array dp[n+1][n+1] with -1.

4. Define recursive function lps(s1, s2, n1, n2):

5. If n1 == 0 or n2 == 0: return 0.

6. If dp[n1][n2] != -1: return it.

7. If s1[n1-1] == s2[n2-1]: dp[n1][n2] = 1 + lps(s1, s2, n1-1, n2-1)

8. Else: dp[n1][n2] = max(lps(n1-1, n2), lps(n1, n2-1))

9. Call lps(seq[::-1], seq, n, n) to get LPS length.

## Program:

Program to implement to find the length of the longest palindromic subsequence in it

Developed by:Vidhyasri k

Register Number: 212222230170

```
dp = [[-1 for i in range(1001)]for j in range(1001)]
def lps(s1, s2, n1, n2):
    if (n1 == 0 or n2 == 0):
        return 0
    if (dp[n1][n2] != -1):
        return dp[n1][n2]
    if (s1[n1 - 1] == s2[n2 - 1]):
        dp[n1][n2] = 1 + lps(s1, s2, n1 - 1, n2 - 1)
        return dp[n1][n2]
    else:
        dp[n1][n2] = max(lps(s1, s2, n1 - 1, n2), lps(s1, s2, n1, n2 - 1))
        return dp[n1][n2]
seq = input()
n = len(seq)
s2 = seq
s2 = s2[::-1]
print(f"The length of the LPS is",lps(s2, seq, n, n))
```

## Output:

![image](https://github.com/user-attachments/assets/bc52eb80-990c-4587-996a-4f7238f8e298)


## Result:
Thus the program was executed successfully for finding the length of longest palindromic string.
