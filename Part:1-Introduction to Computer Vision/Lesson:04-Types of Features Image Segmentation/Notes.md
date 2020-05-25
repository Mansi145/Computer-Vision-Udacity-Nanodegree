### Types of features -
- Edges
- Corners (easiest to identify)
- Blobs

_Try working on binsry images (B/W) for best results_
### Corner Detection - 
Abrupt change (gradient) in any single direction. First the gradient magnitude is calculated in every direction. Both can be calculated by any operator such as Sobel Operator.
#### Sobel Filter - 
Image coordinates to Polar coordinates. Gradients in x and y direction are used to calculate Gradient Magnitude. 

`rho = sqrt(Gx^2 + Gy^2)`

### Dilation and Erosion
Dilation and erosion are known as morphological operations. They are often performed on binary images, similar to contour detection. Dilation enlarges bright, white areas in an image by adding pixels to the perceived boundaries of objects in that image. Erosion does the opposite: it removes pixels along object boundaries and shrinks the size of objects.

Often these two operations are performed in sequence to enhance important object traits!
```
# Reads in a binary image
image = cv2.imread(‘j.png’, 0) 

# Create a 5x5 kernel of ones
kernel = np.ones((5,5),np.uint8)

# Dilate the image
dilation = cv2.dilate(image, kernel, iterations = 1)

# Erode the image
erosion = cv2.erode(image, kernel, iterations = 1)
```

<img src="https://i.ytimg.com/vi/uUweXBmm978/maxresdefault.jpg" width=500>
<img src="https://imagej.net/_images/thumb/f/f2/Principle-of-morphological-dilation-and-erosion.png/700px-Principle-of-morphological-dilation-and-erosion.png" width=600>

### Opening
These operations are often combined for desired results! One such combination is called opening, which is erosion followed by dilation. This is useful in noise reduction in which erosion first gets rid of noise (and shrinks the object) then dilation enlarges the object again, but the noise will have disappeared from the previous erosion!

<img src="https://www.dspguide.com/graphics/F_25_10.gif" width=500>
<img src="https://answers.opencv.org/upfiles/1398619945496278.png" width=500>
<img src="https://miro.medium.com/max/3126/1*nFSDk96bRCB2xx1W_qggAw.png" width=500>

### Image Segmentation 
