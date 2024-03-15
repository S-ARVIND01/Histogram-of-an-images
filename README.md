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
Developed By: ARVIND S
Register Number: 212222240012
```
## Input Grayscale Image and Color Image :
```python
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("eagle.jpeg")
color_image = cv2.imread("stone.jpg")
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Color Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Histogram of Grayscale Image and any channel of Color Image :
```python
import numpy as np
import cv2
Gray_image = cv2.imread("eagle.jpeg")
Color_image = cv2.imread("stone.jpg")
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
## Histogram Equalization of Grayscale Image :
```python
import cv2
gray_image = cv2.imread("eagle.jpeg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
### Input Grayscale Image and Color Image
![Screenshot 2024-03-15 191746](https://github.com/S-ARVIND01/Histogram-of-an-images/assets/118707337/d9acddb8-e3f2-4ee9-b63e-8f8678dbc8f2)
![Screenshot 2024-03-15 191809](https://github.com/S-ARVIND01/Histogram-of-an-images/assets/118707337/ebd6a95d-8b02-401f-8319-60804b59f37c)

### Histogram of Grayscale Image and any channel of Color Image
#### Gray Scale -
![image](https://github.com/S-ARVIND01/Histogram-of-an-images/assets/118707337/bf6ed934-629b-4db4-a1c9-5a8c1731458b)

![image](https://github.com/S-ARVIND01/Histogram-of-an-images/assets/118707337/7bf24782-b1e8-4532-867b-94e16adf54e8)
#### Colour Image -
![image](https://github.com/S-ARVIND01/Histogram-of-an-images/assets/118707337/0c36098b-e4d1-4162-b647-e8d778e10e11)

![image](https://github.com/S-ARVIND01/Histogram-of-an-images/assets/118707337/f95bb9c6-41ab-4b75-9e5a-26070ebccd42)

### Histogram Equalization of Grayscale Image.
![Screenshot 2024-03-15 192008](https://github.com/S-ARVIND01/Histogram-of-an-images/assets/118707337/ce410aab-942c-434c-b71b-60cff1ed818e)

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
