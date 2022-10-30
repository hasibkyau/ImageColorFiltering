import cv2
from matplotlib import pyplot as plt
import numpy as np
import matplotlib.image as mpimg

img = mpimg.imread('../input/myData/rolex.jpg')

hsv = cv2.cvtColor(img, cv2.COLOR_BGR2HSV)
    
lower_red = np.array([30,150,50])
upper_red = np.array([255,255,180])
    
mask = cv2.inRange(hsv, lower_red, upper_red)
res = cv2.bitwise_and(img, img, mask= mask)

# plt.imshow(img)
# plt.imshow(hsv)

fig=plt.figure(figsize=(15,15))
fig.add_subplot(1,3,1)
plt.imshow(img)

fig.add_subplot(1,3,2)
plt.imshow(mask)

fig.add_subplot(1,3,3)
plt.imshow(res)
plt.show()
