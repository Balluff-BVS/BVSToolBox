# <p align="right"><a class="github-button" aria-label="Download ntkme/github-buttons on GitHub" href="https://github.com/Balluff-BVS/halconscripts/raw/master/Filters/Points/points_filters.zip" data-icon="octicon-cloud-download">Download</a></p>


POINTS FOERSTNER
==========

## Example

Original Picture             | Filtered Picture
:-------------------------:|:-------------------------:
![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Filters/Points/PointsFoerstner/original.png?raw=true)  |  ![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Filters/Points/PointsFoerstner/points_foerstner.png?raw=true)

Description
----------

Detect points of interest using the Förstner operator.

Significant points are points that differ from their neighborhood, i.e., points where the image function changes in two dimensions. These changes occur on the one hand at the intersection of image edges (called junction points), and on the other hand at places where color or brightness differs from the surrounding neighborhood (called area points).

Input Parameters
----------

**SigmaGrad** - Amount of smoothing used for the calculation of the gradient. If *Smoothing* is 'mean', SigmaGrad is ignored.

*Default value:* 1

*Suggested values:* 0.7, 0.8, 0.9, 1.0, 1.2, 1.5, 2.0, 3.0

**SigmaInt** - Amount of smoothing used for the integration of the gradients.

*Default value:* 2

*Suggested values:* 0.7, 0.8, 0.9, 1.0, 1.2, 1.5, 2.0, 3.0

**SigmaPoints** - Amount of smoothing used in the optimization functions.

*Default value:* 3

*Suggested values:* 0.7, 0.8, 0.9, 1.0, 1.2, 1.5, 2.0, 3.0

**ThreshInhom** - Threshold for the segmentation of inhomogeneous image areas.

*Default value:* 200

*Suggested values:* 50, 100, 200, 500, 1000

**ThreshShape** - Threshold for the segmentation of point areas.

*Default value:* 0.3

*Suggested values:* 0.1, 0.2, 0.3, 0.4, 0.5, 0.7

**Smoothing** - Used smoothing method.

*Default value:* 'gauss'

*List of values:* 'gauss', 'mean'

**EliminateDoublets** - Elimination of multiply detected points.

*Default value:* 'false'

*List of values:* 'false', 'true'


