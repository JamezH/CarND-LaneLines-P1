# **Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./examples/grayscale.jpg "Grayscale"

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of these step:

    Converting from RPG to HSV. This allows the computer to pick up the colors better without variances from lightning and shading.
    An Gaussian blur to blur up the images so the contrast is not too sharp for Canny edge.
    Canny edge detection to pickup edges to make lines using hough transform.
    Filter color to only pick up white and yellow.
    Defining a region of interest to only look at where the road usually is but distorted to the camera view.
    Finally the hough transform makes lines of the edges.






### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when going over bridges with light colors. In the optional bridge.

Another short coming is if there is distortion in the camera. For example using a wide-angle lens camera. It will not process it well.  


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to add an calibration step for the camera to adjust for constant distortions.
