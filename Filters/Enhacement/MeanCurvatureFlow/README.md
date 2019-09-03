# <p align="right"><a class="github-button" aria-label="Download ntkme/github-buttons on GitHub" href="https://github.com/Balluff-BVS/halconscripts/raw/master/Filters/Enhacement/enhancement_filters.zip" data-icon="octicon-cloud-download">Download</a></p>

MEAN CURVATURE FLOW
==========

## Example

Original Picture             | Filtered Picture
:-------------------------:|:-------------------------:
![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Filters/Enhacement/MeanCurvatureFlow/original.png?raw=true)  |  ![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Filters/Enhacement/MeanCurvatureFlow/mean_curvature_flow.png?raw=true)

Description
----------

Causes a smoothing of image in the direction of the edges in the image, i.e. along the contour lines, while perpendicular to the edge direction no smoothing is performed and hence the boundaries of image objects are not smoothed. 

To detect the image direction more robustly, in particular on noisy input data, an additional isotropic smoothing step can precede the computation of the gray value gradients. The parameter *Sigma* determines the magnitude of the smoothing by means of the standard deviation of a corresponding Gaussian convolution kernel.

Input Parameters
----------

**Sigma** - Smoothing for derivative operator.

*Default value:* 0.5

*Suggested values:* 0.0, 0.1, 0.5, 1.0

*Restriction:* 0 <= Sigma

**Theta** - Time step.

*Default value:* 0.5
 
*Suggested values:* 0.1, 0.2, 0.3, 0.4, 0.5

*Restriction:* 0 <= Theta <= 0.5

**Iterations** - Number of iterations.

*Default value:* 10
 
*Suggested values:* 1, 5, 10, 20, 50, 100, 500

**Restriction:* 1 <= Iterations
