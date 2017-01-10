# Python_Data_Scientist_Scripts

## Common Imports
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
###Plotting
* In order to display a grey image, we have to explicitly say so: 
```
figure = plt.imshow(screen, cmap=plt.cm.Greys_r)
```
