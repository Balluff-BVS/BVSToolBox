# <p align="right"><a class="github-button" aria-label="Download ntkme/github-buttons on GitHub" href="https://github.com/Balluff-BVS/halconscripts/raw/master/Filters/Points/points_filters.zip" data-icon="octicon-cloud-download">Download</a></p>


POINTS HARRIS
==========

## Example

Points Harris             | Points Harris Binomial
:-------------------------:|:-------------------------:
![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Filters/Points/PointsHarris/points_harris.png?raw=true)  |  ![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Filters/Points/PointsHarris/points_harris_binomial.png?raw=true)

Description
----------

**points_harris** - Detect points of interest using Harris operator.

**points_harris_binomial** - Detect points of interest using the binomial approximation of the Harris operator.

Input Parameters
----------

**Alpha** - Weight of the squared trace of the squared gradient matrix.

*Default value:* 0.08

*Suggested values:* 0.02, 0.03, 0.04, 0.05, 0.06, 0.07, 0.08

**Threshold** - Minimum filter response for the points.

*Default value:* 1000

*Restriction:* Threshold >= 0

**Parameters for *points_harris* only:**

**SigmaGrad** - Amount of smoothing used for the calculation of the gradient.

*Default value:* 0.7

*Suggested values:* 0.7, 0.8, 0.9, 1.0, 1.2, 1.5, 2.0, 3.0

**SigmaSmooth** - Amount of smoothing used for the integration of the gradients.

*Default value:* 2

*Suggested values:* 0.7, 0.8, 0.9, 1.0, 1.2, 1.5, 2.0, 3.0

**Parameters for *points_harris_binomial* only:**

**MaskSizeGrad** - Amount of binomial smoothing used for the calculation of the gradient.

*Default value:* 5

*Suggested values:* 3, 5, 7, 9, 11, 15, 21, 31

**MaskSizeSmooth** - Amount of smoothing used for the integration of the gradients.

*Default value:* 15

*Suggested values:* 3, 5, 7, 9, 11, 15, 21, 31

**Subpix** - Turn on or off subpixel refinement.

*Default value:* 'on'

*Suggested values:* 'off', 'on'
