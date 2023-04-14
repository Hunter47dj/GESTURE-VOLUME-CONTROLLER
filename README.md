<!-- MADE BY DHARMENDRA CHOUDHARY -->

# Gesture Volume Control

Gesture Volume Control is the about changing the volume according to the movement of fingers. The volume changes as the distance between the index finger and thumb varies.

# Libraries used

opencv-contrib-python 4.7.0.72

mediapipe 0.9.1.0

pycaw 20220416

# Module 1 - HandTrackingModule

This module deals with tracking the movement of hand. This also highlights the 21 landmarks which are defined by Google in Mediapipe. 

This consists of two functions - findHand and findPosition

## findHand

This function after converting the BGR image to RGB highlights the 21 landmarks on your hand along with connections of these landmarks.

## findPosition

This function is used to get the position of a particular landmark on your hand and also highlights it by drawing circle on it.

# Module 2 - VolumeControl

This module executes our main motive. This first detects the movement of hand. After that you need to pass the landmark number of index finger (8) and thumb (4) as specified by Google. It then calulates the distance between the index finger and thumb by using the hypot method of math module. Also you can calulate the mid point of the line joining these two, which changes it's color below a certain range. 

Note - You need to check the range of the length of line between the index finger and thumb before connecting the change of volume with length. 

check the volume range by printing the GetVolumeRange to make the conversions. 

To make the conversion use the interp method from numpy library, keeping in mind the ranges that you have got. 

If you want to display the volume bar, you can do this by calling the rectangle method of opencv library and giving the desired dimensions to it. 

Congrats you have made the project to change the volume using your hands!!



