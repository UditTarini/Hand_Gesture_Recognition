# Hand_Gesture_Recognition

## Description
This project implements Computer Vision techniques to perform hand gesture recognition. 
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


