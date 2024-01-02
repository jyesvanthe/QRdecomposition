## EX-08: Algorithm for QR Decomposition
## Aim:
To implement QR decomposition algorithm using the Gram-Schmidt method.

## Equipment’s required:
Hardware – PCs
Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
1.Intialize the matrix Q and u
2.The vector u and e is given by
![image](https://github.com/jyesvanthe/QRdecomposition/assets/150319392/dd2d1e18-a324-4d65-9d36-fdee2a436521)

3.Obtain the Q matrix

![image](https://github.com/jyesvanthe/QRdecomposition/assets/150319392/a401177d-1f89-4207-9b97-dc591994a08b)

4.Construct the upper triangular matrix R
![image](https://github.com/jyesvanthe/QRdecomposition/assets/150319392/d64ed45c-fd65-4840-9fe9-826f1785cfe4)

## Program:
```
Gram-Schmidt Method
'''
Program to QR decomposition using the Gram-Schmidt method
Developed by: KEERTHANA S
RegisterNumber: 23013398
'''
import numpy as np
def QR_Decomposition(A):
    n,m = A.shape
    Q=np.empty((n,n))
    u=np.empty((n,n))
    u[:,0] = A[:,0]
    Q[:,0] = u[:,0]/np.linalg.norm(u[:,0])
    for i in range(1,n):
        u[:,i]=A[:,i]
        for j in range(i):
            u[:,i]-=(a[:,i]@Q[:,j])*Q[:,j]
        Q[:,i] = u[:,i]/np.linalg.norm(u[:,i])
    R=np.zeros((n,m))
    for i in range(n):
        for j in range(i,m):
            R[i,j]=a[:,j]@Q[:,i]
    print(Q)        
    print(R)
    
a = np.array(eval(input()))
QR_Decomposition(a)
```
## Output
![image](https://github.com/jyesvanthe/QRdecomposition/assets/150319392/05764d5e-f4af-429f-b3cf-0cbb14654c42)

## Result
Thus the QR decomposition algorithm using the Gram-Schmidt process is written and verified the result.

