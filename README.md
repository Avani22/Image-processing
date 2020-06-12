# Image-processing

Step 1: Sampling 

•	Before doing any experiment, we make sure that we use gray scale normalized image, i.e., image intensity range between [0; 1]. 
•	Implemented my own function to downsample an image into half size (for x and y directions) by sampling every other pixel. 
•	Performed downsampling twice on ‘lena.png’. 
•	Compared the downsampled images with the original in the same actual size (pixel size for low resolution images should be bigger.)
•	 Again, performed upsampling of the image by inserting an empty pixel between every and each pixel. Ran it twice to get it back to the original size.

Step 2: Gaussian Smoothing

•	Implemented a function that takes in an image I, kernel size k and scal-ing parameter s (i.e., ) and outputs its smoothed version after Gaussian smoothing, i.e., I smooth = myGaussianSmoothing(I, k, s). 
•	Tested it on the given image ‘lena.png’. 
•	Changed the kernel size to k = f3; 5; 7; 11; 51g with xed s = 1. 
•	Again, changed the s = f0:1; 1; 2; 3; 5g with xed kernel size k = 11. 

Step 3: Image Filtering

•	Solved the problem that occurred from sampling by using Image filtering. 
•	Everytime after performing upsampling, performed Gaussian smoothing with k = 11 and = 1.
•	Implemented my own median filter function and applied it on the same upsampled data. 

Step 4: Gaussian Noise

•	On the original ‘lena.png’ image, added some Gaussian noise N(0; 0:1) at each pixel, i.e., I noisy(x; y) = I(x; y) + r where r N(0; 0:1). 
•	 Performed Gaussian smoothing. 
•	Applied median filtering on it.
•	Changed the type of noise I added before. 
•	Set the noise to value 1 everywhere where the noise was > 0:2 and 0 otherwise. 
•	Applied Gaussian smoothing. Then applied median filtering as well on it.

Step 5: Sobel Filter

•	Implemented a Sobel filter that calculates gradient along x and y directions. 
•	To visualize the sobel operator, normalize the gradients so that all the values lie between [0,1]. 
•	My function looks like [mag, ori] = mySobelFilter(I) that takes an image I as an input and output edge response (magnitude) and orientation for each pixel.
•	 Visualized the result in color by using the magnitude to specify the saturation and value of an image and the orientation to specify the hue. 

