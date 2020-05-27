## Feature Vectors 
Gradient vectors in a training image forms a pattern to recognize it in other testing images. Say we want a way to detect this mountain in other images, too. A single corner will not be enough to identify this mountain in any other images, but, we can take a set of features that define the shape of this mountain, group them together into an array or vector, and then use that set of features to create a mountain detector!

<img src="https://github.com/Mansi145/Computer-Vision-Udacity-Nanodegree/blob/master/Images/sdfgh.PNG" width=500>
<img src="https://github.com/Mansi145/Computer-Vision-Udacity-Nanodegree/blob/master/Images/dwjhdwd.PNG" width=500>

## Real time feature detection 
### [ORB Algorithm](https://medium.com/data-breach/introduction-to-orb-oriented-fast-and-rotated-brief-4220e8ec40cf)
Oriented FAST and Rotated BRIEF
ORB is basically a fusion of FAST keypoint detector and BRIEF descriptor with many modifications to enhance the performance.

<img src="https://github.com/Mansi145/Computer-Vision-Udacity-Nanodegree/blob/master/Images/hgh.PNG" width=700>
<img src="https://github.com/Mansi145/Computer-Vision-Udacity-Nanodegree/blob/master/Images/dfghjk%2C.PNG" width=700>

**FAST** = Features from Accelerated Segments Test - To find the keypoints by comparing the brightness levels in a pixel area (the second image). For ex we only need to caompare 'p' with the pixels 1, 5, 9, 13. This methods reduces the time factor by 4 compared to the traditional methods of comparing every pixel. These keypoints are located in a change of intensity whish is usually an edge of some kind like the cats eyes or the paws. But this only gives us an edge without giving us any info about the direction of change of intensity so we cannot distinguish between horizontal or veritical edges.

**BRIEF** - Binary Robust Independent Elementary Features - Brief takes all keypoints found by the fast algorithm and convert it into a binary feature vector so that together they can represent an object. The Binary Vectors given in the first image are the Feature Vectors. Brief start by smoothing image using a Gaussian kernel in order to prevent the descriptor from being sensitive to high-frequency noise. 
<img src="https://miro.medium.com/max/1400/1*8v4ZvgwE0DYiCzQDRvno1A.png">
