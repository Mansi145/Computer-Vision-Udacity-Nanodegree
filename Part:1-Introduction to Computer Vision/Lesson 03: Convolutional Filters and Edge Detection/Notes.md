### Intensity 
Intensity is a measure of light and dark similar to brightness, and we can use this knowledge to detect other areas or objects of interest.
For example, you can often identify the edges of an object by looking at an abrupt change in intensity which happens when an image changes from a very dark to light area.

### Filters 
To detect these changes, you’ll be using and creating specific image filters that look at groups of pixels and detect big changes in intensity in an image. These filters produce an output that shows these edges.

## Frequency in Images 
### Frequency - 
We have an intuition of what frequency means when it comes to sound. High-frequency is a high pitched noise, like a bird chirp or violin. And low frequency sounds are low pitch, like a deep voice or a bass drum. For sound, frequency actually refers to how fast a sound wave is oscillating; oscillations are usually measured in cycles/s (Hz), and high pitches and made by high-frequency waves.

### Fourier Transformation in Images - 
The Fourier Transform is an important image processing tool which is used to decompose an image into its sine and cosine components.The output of the transformation represents the image in the Fourier or frequency domain, while the input image is the spatial domain equivalent. In the Fourier domain image, each point represents a particular frequency contained in the spatial domain image.
![Image1](https://github.com/Mansi145/Computer-Vision-Udacity-Nanodegree/blob/master/Images/ggvhgv.PNG)
![Image2](https://github.com/Mansi145/Computer-Vision-Udacity-Nanodegree/blob/master/Images/hjk%2C.PNG)
Lower frequencies contains image details.

## Filtering - 
* Filter out unwanted noise
* Amplify certain features (High Pass Filter)
### High Pass vs Low Pass Filter -  
![](https://github.com/Mansi145/Computer-Vision-Udacity-Nanodegree/blob/master/Images/images.jpg)
#### High Pass - 
* Sharpen an Image
* Enahance High Frequency parts of the image
