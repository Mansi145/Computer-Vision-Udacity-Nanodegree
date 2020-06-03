### Cognitive and Emotional Intelligence
**Cognitive intelligence** is the ability to reason and understand the world based on observations and facts. It's often what is measured on academic tests and what's measured to calculate a person's IQ.

**Emotional intelligence** is the ability to understand and influence human emotion. For example, observing that someone looks sad based on their facial expression, body language, and what you know about them - then acting to comfort them or asking them if they want to talk, etc. For humans, this kind of intelligence allows us to form meaningful connections and build a trustworthy network of friends and family. It's also often thought of as only a human quality and is not yet a part of traditional AI systems.

### Standardizing Data
![](https://github.com/Mansi145/Computer-Vision-Udacity-Nanodegree/blob/master/Images/screen-shot-2018-04-23-at-4.05.20-pm.png)
If the images are different sizes, or even cropped differently, then this counting tactic will likely fail! So, it's important to pre-process these images so that they are standardized before they move along the pipeline. In the example below, you can see that the images are pre-processed into a standard square size.
![](https://github.com/Mansi145/Computer-Vision-Udacity-Nanodegree/blob/master/Images/stop-sign-classification.png)

### Neural Nets vs Dense Neural Nets
**Neural Nets** - Only a single layer
![](https://github.com/Mansi145/Computer-Vision-Udacity-Nanodegree/blob/master/Images/screen-shot-2018-03-23.png) </br>
**Dense Neural Nets** - Layer of separation i.e. having multiple layers of separation.
![](https://github.com/Mansi145/Computer-Vision-Udacity-Nanodegree/blob/master/Images/screen-shot-2018-03-23.png)

### Why OpenCV reads images in BGR?
When OpenCV was first being developed, BGR color format was popular among camera manufacturers and image software providers. The red channel was considered one of the least important color channels, so was listed last, and many bitmaps use BGR format for image storage. However, now the standard has changed and most image software and cameras use RGB format, which is why, in these examples, it's good practice to initially convert BGR images to RGB before analyzing or manipulating them.

### Understanding Color Spaces
![](https://github.com/Mansi145/Computer-Vision-Udacity-Nanodegree/blob/master/Images/a-the-RGB-color-space-black-arrows-show-the-three-main-color-dimensions-whose-values.jpg)
The lumination will be taken in account by the **Value** in HSV. Think of it as shade. HSL will be studied later.

[Color Reference](https://www.w3schools.com/colors/colors_picker.asp)

### Standardizing Labels 
- Categorical Label - [cat value, tiger value, hippopotamus value, dog value]
- Numerical Label
  - Integer encoding - [0,1,2,3]
  - One hot-encoding - [[1,0,0,0], [0,1,0,0], [0,0,1,0], [0,0,0,1]] **One-hot encoding is often used when there are more than 2 values to separate**
Categorical labels are descriptive for us, but may be inefficient for a classification task. Many machine learning algorithms do not; they require that all output be numerical. Numbers are easily compared and stored in memory.\

### Average Brightness of an Image
Used for day/night classification. Steps followed are - 
1. Convert the image to HSV color space (the Value channel is an approximation for brightness)
2. Sum up all the values of the pixels in the Value channel
3. Divide that brightness sum by the area of the image, which is just the width times the height.
4. This gave us one value: the average brightness or the average Value of that image.

