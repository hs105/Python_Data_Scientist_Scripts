# Python_Data_Scientist_Scripts

## Common Imports
This documdent uses the following imports:
```
import numpy as np
import matplotlib.pyplot as plt
```

## Machine Learning Algorithms

### Expectation Maximization

### Collaborative Filtering

### Kalman Filter

### Particle Filter


### Array

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

* Root Mean Square Error (so-called RMSE). Say predictions and targets are two vectors (1D array), you can calculate the RMSE by:
```
np.sqrt(np.mean((predictions-targets)**2))
```

###Plotting

* In order to display a grey image, we have to explicitly say so: 
```
figure = plt.imshow(grey_image, cmap=plt.cm.Greys_r)
```

* Real time plotting: plotting a sequence of images so it looks a video. Just generate the figure in the beginning and set the figure's data to the image. In a game playing setting, this looks like
```
import matplotlib.pyplot as plt

def play_one_game(agent):
    agent.game.new_episode()
    n = 0
    while not agent.game.is_finished() and n < 200:
        screen_image = agent.game.state()
        agent.observe_state(screen_image)
        if n == 0:
            figure = plt.imshow(screen_image, cmap=plt.cm.Greys_r)
        else:
            figure.set_data(screen_image)
            plt.pause(0.01)
        a, r, _ = agent.act()
        n += 1
    return total_rewards, n
```
"screen_image" is a 2D array image. What shows here is a plotting in grey mode. 

### GPU
To find your display card on ubuntu, 
```
lspci | grep VGA
```
Hope you see Nvidia cards. Right now [OpenCV (version 3) only supports NVIDIA GPUs](http://docs.opencv.org/2.4/modules/gpu/doc/introduction.html). 

