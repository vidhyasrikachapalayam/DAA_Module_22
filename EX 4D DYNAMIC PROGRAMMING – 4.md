# EX 4D DYNAMIC PROGRAMMING – 4

## DATE:  12/04/25

## AIM:
To find the minimum number of operations to convert str1 to str2 using Naive recursive method.

## Algorithm

1. Input two strings s and t.

2. Base Cases:

   If s is empty, return len(t).

   If t is empty, return len(s).

3. If last characters match: Set cost = 0

4. Else: Set cost = 1

5. Recursive Step:

   Return minimum of:

     1 + LD(s[:-1], t) (delete)

     1 + LD(s, t[:-1]) (insert)

     cost + LD(s[:-1], t[:-1]) (substitute)
   
## Program:

Program to implement to find the minimum number of operations to convert str1 to str2 using Naive recursive method

Developed by: Vidhyasri k

Register Number: 212222230170

```
def LD(s, t):
    
    if s == "":
        return len(t)
    if t == "":
        return len(s)
    if s[-1] == t[-1]:
        cost = 0
    else:
        cost = 1
    res = min([LD(s[:-1], t)+1, LD(s, t[:-1])+1, LD(s[:-1], t[:-1]) + cost])
    return res
    
str1=input()
str2=input()
print('Edit Distance',LD(str1,str2))

```

## Output:

![image](https://github.com/user-attachments/assets/97d78c0b-4d3f-4f27-9ad5-dd0d57a61989)


## Result:
Thus the program was executed successfully for finding edit distance between two strings.
