#**Finding Lane Lines on the Road** 


### Reflection

###1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 5 steps:

- Convert the images to gray scale
- Perform Gausian smoothing and apply Canny edge detection
- Select region of interest and mask other areas of the image
- Apply Hough Transform to detect lane lines
- Superimpose the lane lines on the original image

In order to draw a single line for both lane, I modified the draw_lines() function by:

- Calculated slope and center of each line. Then based on the slope, sort it into right or left lane line
- Calculate the average slope and the center of right and left lane
- Then using the Y coordinates, based on Region of Interest, figure out the X coordinates using the avg slope and center point of lane lines.


###2. Identify potential shortcomings with your current pipeline


It looks like my pipeline doesnt really work for challenge which contains curve.


###3. Suggest possible improvements to your pipeline

Modify the slope conditions, so that they work with curve in the road