# Algorithm for QR Decomposition
## Aim:
To implement QR decomposition algorithm using the Gram-Schmidt method.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
1.	Intialize the matrix Q and u
2.	The vector u and e is given by

    ![eqn1](./ex4.jpg)

    ![eqn2](./ex6.jpg)

    ![eqn3](./ex3.jpg)

3.	Obtain the Q matrix   
    ![eqn4](./ex1.jpg)
4.	Construct the upper triangular matrix R
    ![eqn5](./ex2.jpg)



## Program:
### Gram-Schmidt Method
```
A = eval(input())

cols = len(A[0])
max_sum = 0

for j in range(cols):
    s = 0
    for i in range(len(A)):
        s += abs(A[i][j])
    if s > max_sum:
        max_sum = s

print("{:.2f}".format(max_sum))

A = eval(input())

m = len(A)
n = len(A[0])

B = [[0 for j in range(n)] for i in range(n)]

for i in range(n):
    for j in range(n):
        s = 0
        for k in range(m):
            s += A[k][i] * A[k][j]
        B[i][j] = s

trace = B[0][0] + B[1][1]
det = B[0][0] * B[1][1] - B[0][1] * B[1][0]

eigen = ((trace + (trace**2 - 4*det) ** 0.5) / 2) ** 0.5

print("{:.2f}".format(eigen))



A = eval(input())

max_sum = 0

for i in range(len(A)):
    s = 0
    for j in range(len(A[0])):
        s += abs(A[i][j])

    if s > max_sum:
        max_sum = s

print("{:.2f}".format(max_sum))


 



```

## Output
```
<img width="546" height="477" alt="image" src="https://github.com/user-attachments/assets/086eb816-7aed-49c3-821f-bb765232bb8f" />
<img width="632" height="528" alt="image" src="https://github.com/user-attachments/assets/3e807f44-865d-40d5-a149-562da50abccd" />
<img width="411" height="398" alt="image" src="https://github.com/user-attachments/assets/a838646e-99fe-476d-8b33-905ddbe9f20d" />

```

## Result
Thus the QR decomposition algorithm using the Gram-Schmidt process is written and verified the result.
