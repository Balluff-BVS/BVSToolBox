# <p align="right"><a class="github-button" aria-label="Download ntkme/github-buttons on GitHub" href="https://github.com/Balluff-BVS/halconscripts/raw/master/Filters/Edges/edges_filters.zip" data-icon="octicon-cloud-download">Download</a></p>


SOBEL OPERATOR
==========

## Example

Edges Amplitude             | Edges Direction
:-------------------------:|:-------------------------:
![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Filters/Edges/Sobel/sobel_amp.png?raw=true)  |  ![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Filters/Edges/Sobel/sobel_dir.png?raw=true)

Description
----------

Calculate an approximation of the first derivative of the image data and is used as an edge detector.

**sobel_amp** - detects edges amplitude

**sobel_dir** - detects edges both amplitude and direction

Input parameters
---------------

**Size** - Size of filter mask.

*Default value:* 3

*List of values:* 3, 5, 7, 9, 11, 13, 15, 17, 19, 21, 23, 25, 27, 29, 31, 33, 35, 37, 39

**FilterType** - Filter type.

*Default:* 'sum_abs'

*List of values:*  'sum_abs', 'sum_abs_binomial', 'sum_sqrt', 'sum_sqrt_binomial'
