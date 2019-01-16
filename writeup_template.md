# **Finding Lane Lines on the Road** 

## Writeup Template

### You can use this file as a template for your writeup if you want to submit it as a markdown file. But feel free to use some other method and submit a pdf if you prefer.

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./examples/grayscale.jpg "Grayscale"

---

### Reflection

1, filter out yellow and white color by cv.inrange(), convert to hsv image

2, set the vertices  as np.array([[(0, imshape[0]), (imshape[1]*2/5, imshape[0]*5/8),
    (imshape[1]*3/5, imshape[0]*5/8), (imshape[1],imshape[0])]], dtype=np.int32) instead of fixing
vertices

3, do the course test code do

4, average left, right line's m and b. And recalculate the two line, draw with thickness=8

Potential Shortage and possible improvements:

The vertices range might not robust enough, it's very depended on camera position and angle in car.

And it might have a smooth function for video processing.

for the merged lane or not regualr two parallel lanes, cannot work well.
