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
# Developed By: Sabeeha Shaik
# Register Number: 212223230176
```
## Output:
### Input Grayscale Image and Color Image
```
import cv2
from matplotlib import pyplot as plt
# Load the color image
image = cv2.imread('beach.jpg')
# Convert the image to grayscale
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')
```
![image](https://github.com/user-attachments/assets/514c1493-c0b7-4d1e-8f76-195fc9a98aa4)


### Histogram of Grayscale Image and any channel of Color Image
```
hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])
plt.plot(hist_original, color='black')
plt.title('Original Histogram')
plt.xlim([0, 256])
```
![image](https://github.com/user-attachments/assets/2c75e9d6-472c-4876-9284-1f7676efe222)

### Equalization
```
hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])
plt.plot(hist_original, color='black')
plt.title('Original Histogram')
plt.xlim([0, 256])
```
![image](https://github.com/user-attachments/assets/93bb79ed-d36a-4bf4-b9b7-ee0f06e80c2d)


### Histogram Equalization of Grayscale Image.
```
hist_original = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])
plt.plot(hist_original, color='black')
plt.title('Equalized Histogram')
plt.xlim([0, 256])
```
![image](https://github.com/user-attachments/assets/de8fe5c8-706d-4fb5-8885-a0700d2c24ef)



## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
