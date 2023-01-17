# NumPy-Lab2
#1 Q1: Import numpy library
import numpy as np 

#2 Q2: Generate a sequence of 15 floats using linspace() function
np.linspace(0,15)

#3 Q3: Create a 3-D array in shape (2, 2, 3) containing the four arrays given below
a3D=np.array([[[1.1,2.1,3.1],[4.1,5.1,6.1]],[[7.1,8.1,9.1],[10.1,11.1,12.1]]])
a3D

#4 Q4: Print the following:
print('type = ', a3D.dtype)
print('number of dimensions = ', a3D.ndim)
print('shape = ', a3D.shape)
print('size = ', a3D.size)

#5 Q5: Change the array dimention from 3-D to 4-D
a4D=np.expand_dims(a3D.copy(),axis=0)
a4D

#6
newArr =a4D.copy().astype(int)
newArr

#7
for i in np.nditer(newArr):
  print(i)
  
  #8 
newArr[0,1,0,1]

#9
newArr[0,0,1:,1:]

#10
x= np.where(newArr== 8)
print(x)

#11
newArr.reshape(2,3,2)

#12.1
arr1 = np.array([['A', 'B'], ['E', 'F']])
arr2 = np.array([['C', 'D'], ['G', 'H']])
arr = np.concatenate((arr1, arr2))
arr

#12.2
arr = np.stack([arr1, arr2], axis=1)
arr

#13
arr = np.concatenate((arr1, arr2))
np.split(arr,2,axis=1)

