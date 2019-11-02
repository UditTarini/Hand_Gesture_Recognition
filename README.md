# Hand Gesture Recognition

## Description

These projects demonstrate hand gesture recognition using OpenCV.
Currently, there are two different projects for the recognition of different hand gestures. 
The more detailed explanation about them is given bellow.

The `mouseControler.py` will recognize your fingers and control the mouse according to your finger movements. Basically, it will detect the blue color by specified RGB color range, so you need to stick two red-colored objects to your fingers because the mouse will activate only when it will detect two objects and you need to maintain a certain distance between any two figures then it will calculate the center of those objects. After that, it will find the midpoint of the distance between those points and put a red color point on that. Now the mouse pointer will move according to the red color point. Now the click operation will activate when it detects a single object. So you need to let your fingers close to each other then the program will detect the blue-colored object as a singular object.  Then we can perform some drag and drop at file by a single pinch.
####  Requirements
* ##### OpenCV
   `pip install opencv-python`
* ##### numpy
   `pip install numpy`
* ##### pynput
   `pip install pynput`
* ##### wx
   `pip install -U wxPython`

The `numberCounter.py` will recognise your hand and count the number of fingers. 
This one implements Computer Vision 
techniques to perform hand gesture recognition. 
It will read your hand from a rectangle area which will be cropped to perform filtration 
which is very necessary to get a perfect outline. It performs a Gaussian blur technique to 
filter out the picture. The filtered picture is used to create mask for which it performs 
color detection by restricting itself to find colors within a certain range the range lies 
between the lower and higher HSV value of skin color Now there must be some data loss in our
result so to deal with data loss it performs morphological operations like dilution and erosion 
basically dilation makes the object in white bigger and erosion makes the object in white smaller 
now it needs to detect edge find contours of object so that it can draw a convex hull around it 
Finally for counting the fingers we need to calculate convexity defects the no of convexity defects 
will be found by finding the angle between two fingers, That is if the angle is greater than 90 degree
then we count it
as a defect and number of fingures will be defect+1 and all the angles with less than 90 degrees will be ignored.
### Requirements
* ##### OpenCV
   `pip install opencv-python`
* ##### numpy
   `pip install numpy`
* ##### math
   `pip install mathematics`

