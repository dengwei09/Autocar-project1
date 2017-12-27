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

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 4 steps. First, I converted the images to grayscale, then I use canny function to find the edges on the image. The 3rd step is to find the lines. In order to find lines, Hough transformation is applied to masked image. The original draw_lines() function has been extended to 3 steps:1,left and right lanes have been separated to different containers; and 2,inappropriate lanes are filtered out; 3, connect dotted lines together. After the lines have been found, the four step is to add lines back to original image and print out. 

If you'd like to include images to show how the pipeline works, here is how to include images: 
display(fullpath, imageFiles)
fullpath is the folder location of image files
imageFile is list of the names of image files
![alt text][image1]


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when the lanes are not shown up at appropriate zone. 

Another shortcoming could be inappropriate identification when the lanes are not straight, and when the sunshine is strong. the weakness is obvious in third video(Optional Challenge).  


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to make it more robust to identify curve lanes

Another potential improvement could be to identify lanes on sunshine or other scenarios where the color of lanes is not identifiable.
