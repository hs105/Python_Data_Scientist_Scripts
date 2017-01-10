# Python_Data_Scientist_Scripts

## Common Imports
This documdent uses the following imports:
```
import numpy as np
import matplotlib.pyplot as plt
```

## Root Mean Square Error(RMSE)
Say predictions and targets are two vectors, you can calculate the RMSE by:
```
np.sqrt(np.mean((predictions-targets)**2))
```

## Python

## Array

* To take mean over a dimension (basically this dimension will be reduced)
```
x = np.array([[1.0, 2.0], [-1.0, -2.0]])
y = np.array([[3.0, 4.0], [-3.0, -4.0]])
z = np.array([x, y])
print(z)
print(np.mean(z, 0))
```
The output is 
```
[[[ 1.  2.]
  [-1. -2.]]

 [[ 3.  4.]
  [-3. -4.]]]
[[ 2.  3.]
 [-2. -3.]]
```

* To get the original indices of the sorted array, use the sorted command with a key on the enumerate:
```
a = [-1, 3.3, 2.1]
a_sorted = sorted(a, enumrate(a), key = lambda x: x[1])
print(a_sorted)
```
The output is
```
[(0, -1), (2, 2.1), (1, 3.3)]
```
This trick will be frequently used if you want do some ranking according to some measure. 

###Plotting

* In order to display a grey image, we have to explicitly say so: 
```
figure = plt.imshow(grey_image, cmap=plt.cm.Greys_r)
```

