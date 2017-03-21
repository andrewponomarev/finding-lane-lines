#Finding Lane Lines on the Road

##Writeup


Finding Lane Lines on the Road

The goals / steps of this project are the following:

Make a pipeline that finds lane lines on the road

###1. My pipeline

My pipeline consisted of 5 steps. 
* First, I converted the images to grayscale ;
* Then I apply a gaussian noise kernel to images
* Apply the canny transform to images, which delimit boundaries on the images.
* Apply the image mask, which keeps the region of the image, defined by the polygon, which corresponds to road on the image
* Apply the algorithm, which find hough lines
* Draw this lines on the image

In order to draw a single line on the left and right lanes, I modified the draw_lines() function.
 Function input is list of lines detected on the images. Function distribute lines to left lines with negative slope and to right lines with positive slope. Then it finds mean slope for left line and for right line. On list of left(right) lines and mean slope, function builds one left(right) line.

