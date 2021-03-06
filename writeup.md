# **Finding Lane Lines on the Road** 

---

**Finding Lane Lines on the Road**

This project is the combination of using OpenCV and Python to find the lane line on provided images and then
make annotation on the images. In addition, this program also import the video and find the lane lines then 
make annotation of lane line then out put to the new video file.

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report

---

### Reflection

### 1. Pipeline
The process of finding the lane line on the road are complicated. In order to archieve this result,
I need to process images four steps. First, I converted the image into graysale mode, then I convert to canny 
edge, after that I set the region of the processing image; finally, I draw the left line and right line for the 
line on the road.


In order to draw a single line on the left or right lanes, I modified the draw_lines() function by seperate
left lane and right lane by calculating the slope of the line. From that I have to find the equation that use
to draw the line. From there, I calculate the new extrapolat of the line and draw the new line by using the 
equation.
The pipeline produced the following images:  


![Grayscale](test_videos_output/grayscale.png?raw=true)  
![Canny Edge image](test_videos_output/canny.png?raw=true)  
![Selected Regional Masked Image](test_videos_output/regional_masked.png?raw=true)  
![Annotation Line on Lane Line](test_videos_output/annotationline.png?raw=true)  



### 2. There is potential shortcomings with this current pipeline
There is potential shortcomings with this current pipeline. On the output video from the processing, the annotation on the lane line is shaking. Another shortcoming could be on the different light condition of the road, the program will get error.

### 3. Improvement

A possible improvement would be to adapt to all the light condition on the road. The program should be flexible enough to adapt to all condition of the light on the road.

Another potential improvement could be to have a better calculation so the program could draw the better annotation on the lane line more stable.
