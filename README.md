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
# Developed By: PRASANTH E
# Register Number: 212221233002

import cv2
from matplotlib import pyplot as plt

# Load the color image
image = cv2.imread('ajith.jpg')

# Convert the image to grayscale
gray_image = c
v2.cvtColor(image, cv2.COLOR_BGR2GRAY)

plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')

hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])

# Apply histogram equalization
equalized_image = cv2.equalizeHist(gray_image)

plt.imshow(equalized_image, cmap='gray')
plt.title('Equalized Image')
plt.axis('off')

hist_equalized = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])

plt.plot(hist_equalized, color='black')
plt.title('Equalized Histogram')
plt.xlim([0, 256])



```
## Output:
### Input Grayscale Image and Color Image
![Screenshot 2024-10-01 103123](https://github.com/user-attachments/assets/fb6939f1-7d5b-4e6a-bc42-e48df8e0edf4)


### Histogram of Grayscale Image and any channel of Color Image
![Screenshot 2024-10-01 103146](https://github.com/user-attachments/assets/cf0893d6-d468-42e9-9661-d0c457fdccf5)



### Histogram Equalization of Grayscale Image.
![Screenshot 2024-10-01 103135](https://github.com/user-attachments/assets/9543ad17-dc11-4d51-b853-16cd902d38a2)
![Screenshot 2024-10-01 103159](https://github.com/user-attachments/assets/514c3330-5dfc-4296-a6ad-8104cfc124fb)


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
