# lego-searching

The code was made in MATLAB to count the number of blue rectangles (numA) and number of red squares (numB) on training images.

To initialize the code, download the repository lego-searching, open initialize.m and run the code in MATLAB.


Procedure
1) Download image as I=imread('filename') and invoke count_lego(I) function
2) Use K-Means Clustering to segment the image into different colors
3) Determine which clusters contain blue and red colors
4) Select blue and red clusters containing the most number of blue and red elements, respectively
5) Edge detection using Canny edge detector for red and blue colors
6) Dilation of objects and filling holes
7) Apply watershed method to separate touching objects and determine boundaries of objects
8) Compute properties of each identified object (areas, perimeters, etc.)
9) Classify each object as square/rectangle/circle/triangle
10) If a blue object is rectangular or red object is square, then we can judge whether an object is blue rectangle or red square based on
their perimeters and area properties
11) Count the objects that fall under those categories
