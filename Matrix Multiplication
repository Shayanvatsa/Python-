import numpy as np
import time
def matrix(A,B):
        n=A.shape[0]
        if n==1:
                return A*B
        A11,A12,A21,A22=A[:n//2,:n//2],A[:n//2,n//2:],A[n//2:,:n//2],A[n//2:,n//2:]
        B11,B12,B21,B22=B[:n//2,:n//2],B[:n//2,n//2:],B[n//2:,:n//2],B[n//2:,n//2:]
        C11=matrix(A11,B11)+matrix(A12,B21)
        C12=matrix(A11,B12)+matrix(A12,B22)
        C21=matrix(A21,B11)+matrix(A22,B21)
        C22=matrix(A21,B12)+matrix(A22,B22)
        C=np.zeros((n,n))
        C[:n//2,:n//2],C[:n//2,n//2:],C[n//2:,:n//2],C[n//2:,n//2:]=C11,C12,C21,C22
        return C
n=int(input("enter the size of matrix"))
print("enter matrix A")
A=np.zeros((n,n))
for i in range(n):
        A[i]=list(map(int,input().split()))

print("enter matrix B")
B=np.zeros((n,n))
for i in range(n):
        B[i]=list(map(int,input().split()))
start_time=time.time()
C=matrix(A,B)
end_time=time.time()
print("result:")
print(C)
print("time of execution",end_time-start_time,"seconds")
