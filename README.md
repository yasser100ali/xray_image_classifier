# xray image classifier
A 3part file detailing how to build a convolutional neural network on a set of xray-images. Goal is to predict whether or not each image is 'normal'.
Classes are split into two: 'No Findings' (normal), 'Has Findings'. 

The first file dicom_to_png converts dicom files into png files. This is done in order to reduce the file size. File size is reduced from around 100GB to 1.3GB. 
The original project did not include this step, but training was taking way too long (in excess of 3 days!). This seemed arbitrary given we could easily make this process much faster by simply compressing the file into a png which is around 100 to 200 times smaller! 

The second file transfers each image to the proper subfolder. Subfolder_0 corresponds to images part of class 0, subfolder_1 corresponds to images part of class 1.

The third file builds a model attemting to predict whether or not each x-ray is normal -> 0 or 1. 
