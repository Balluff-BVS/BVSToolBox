# <p align="right"><a class="github-button" aria-label="Download ntkme/github-buttons on GitHub" href="https://github.com/Balluff-BVS/halconscripts/raw/master/Filters/Points/points_filters.zip" data-icon="octicon-cloud-download">Download</a></p>


POINTS LEPETIT
==========

## Example

Original Picture             | Filtered Picture
:-------------------------:|:-------------------------:
![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Filters/Points/PointsLepetit/original.png?raw=true)  |  ![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Filters/Points/PointsLepetit/points_lepetit.png?raw=true)

Description
----------

Extracts points of interest like corners or blob-like structures from image. The image is first smoothed with a median of size 3x3. Then, all the gray values on a circle with radius Radius around an interest point candidate (m) are examined. The absolute differences of two diagonally opposed gray values on the circle to the central pixel m is computed. At least one of these differences has to be larger than *MinCheckNeighborDiff*.

Input Parameters
----------

**Radius** - Radius of the circle.

*Default value:* 3 

*Suggested values:* 3, 5, 6, 7, 8, 9, 10, 15

**CheckNeighbor** - Number of checked neighbors on the circle.

*Default value:* 1

*Suggested values:* 1, 2, 3, 5

**MinCheckNeighborDiff** - Threshold of grayvalue difference to each circle point.

*Default value:* 15

*Suggested values:* 10, 15, 20, 25, 30, 35, 40, 45, 60, 80

**MinScore** - Threshold of grayvalue difference to each circle point.

*Default value:* 30

*Suggested values:* 5, 10, 15, 20, 25, 30

**Subpix** - Subpixel accuracy of point coordinates.

*Default value:* 'interpolation'

*Suggested values:* 'interpolation', 'none'



