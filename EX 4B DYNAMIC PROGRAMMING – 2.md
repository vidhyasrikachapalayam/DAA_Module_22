# EX 4B DYNAMIC PROGRAMMING – 2
## DATE:
## AIM:
To find longest common substring or subword (LCW) of two strings using dynamic programming with bottom-up approach.



## Algorithm
1. Start
2. Input two strings A and B
3. Initialize a variable ans to 0 (this will store the maximum length found)

4. For each index a from 0 to len(A) - 1:
   
       a. For each index b from 0 to len(B) - 1:
   
       i. Initialize k = 0
   
       ii. While both (a + k) < len(A) and (b + k) < len(B), and A[a + k] == B[b + k]:
   
       iii.Increment k by 1
   
       iv. Update ans as the maximum of ans and k

5.Print the value of ans

6.End  

## Program:
```

Program to implement the longest common substring or subword (LCW) of two strings using dynamic programming with bottom-up approach.
Developed by: Vidhyasri K
Register Number: 212222230170

```
```
def LongComSubS(st1, st2):
  ans = 0;
  for a in range(len(st1)):
         for b in range(len(st2)):
            k = 0;
            while ((a + k) < len(st1) and (b + k) < len(st2)
        and st1[a + k] == st2[b + k]):
                k = k + 1;
            ans = max(ans, k);
  return ans;

if __name__ == '__main__':
 
    A = input()
    B = input()
    i = len(A)
    j = len(B)
    print('Length of Longest Common Substring is', LongComSubS(A, B))
```

## Output:
![image](https://github.com/user-attachments/assets/8d3450fc-2975-4c6c-b4a1-6a2aa2f900e7)



## Result:
Thus the program was executed successfully for finding the longest common substring or subword (LCW) of two strings using dynamic programming with bottom-up approach.

