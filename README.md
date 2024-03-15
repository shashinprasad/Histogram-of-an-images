# Histogram-of-an-images
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread()

### Step2:
Print the image using imshow().



### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
The Histogram of gray scale image and color image is shown.


## Program:
```python
# Developed By: Shashin prasad S
# Register Number: 212222230144
```
# Grayscale image and Color image
```
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("immg.jpeg")
color_image = cv2.imread("img.jpeg",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
# Histogram of Grayscale image and color image
```
import numpy as np
import cv2
Gray_image = cv2.imread("immg.jpeg")
Color_image = cv2.imread("img.jpeg")
import matplotlib.pyplot as plt
gray_hist = cv2.calcHist([Gray_image],[0],None,[256],[0,256])
color_hist = cv2.calcHist([Color_image],[0],None,[256],[0,256])
plt.figure()
plt.imshow(Gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale Value")
plt.ylabel("Pixel Count")
plt.stem(gray_hist)
plt.show()
plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)
```
# Histogram equalization of Grayscale image
```
import cv2
gray_image = cv2.imread("immg.jpeg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## Output:
### Input Grayscale Image and Color Image

![Screenshot 2024-03-10 192938](https://github.com/premalatha-sureshbabu/Histogram-of-an-images/assets/120620842/33ef503c-2ac2-4837-b296-4116f8f803d9)

### Histogram of Grayscale Image and any channel of Color Image

![Screenshot 2024-03-12 102721](https://github.com/premalatha-sureshbabu/Histogram-of-an-images/assets/120620842/8af5eb58-65ab-46b2-845e-36be7f8cd901)

![Screenshot 2024-03-12 102740](https://github.com/premalatha-sureshbabu/Histogram-of-an-images/assets/120620842/902d045a-a3dc-4d75-9f1c-2059cac663b8)


### Histogram Equalization of Grayscale Image.

![Screenshot 2024-03-12 102434](https://github.com/premalatha-sureshbabu/Histogram-of-an-images/assets/120620842/bf7aafa7-d9b9-4f86-9926-9ef6c9d15c78)


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
