# <p align="right"><a class="github-button" aria-label="Download ntkme/github-buttons on GitHub" href="https://github.com/Balluff-BVS/halconscripts/raw/master/Filters/Smoothing/BilateralFilter/bilateral_filter.zip" data-icon="octicon-cloud-download">Download</a></p>

BILATERAL FILTER
==========

## Example

Original Picture             | Filtered Picture
:-------------------------:|:-------------------------:
![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Filters/Smoothing/BilateralFilter/original.png?raw=true)  |  ![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Filters/Smoothing/BilateralFilter/bilateral_image.png?raw=true)

Description
----------
The operator applies a shock filter to the input image to sharpen the edges contained in it. To make the edge detection more robust, in particular on noisy images, it can be performed on a smoothed image matrix. This is done by giving the standard deviation of a Gaussian kernel for convolution with the image matrix in the parameter Sigma.

Input Parameters
----------

**Theta** - Time step.

*Default value:* 0.5

*Suggested values:* 0.1, 0.2, 0.3, 0.4, 0.5, 0.6, 0.7

*Restriction:* 0 < Theta <= 0.7


**Iterations** - Number of iterations.

 *Default value:* 10
 
*Suggested values:* 1, 3, 10, 100

*Restriction:* Iterations >= 1


**Mode** - Type of edge detector.

 *Default value:* 'canny'
 
*List of values:* 'canny', 'laplace'


**Sigma** - Smoothing of edge detector.

 *Default value:* 1.0
 
*Suggested values:* 0.0, 0.5, 1.0, 2.0, 5.0

*Restriction:* Theta >= 0


