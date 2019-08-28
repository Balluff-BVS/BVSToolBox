# <p align="right"><a class="github-button" aria-label="Download ntkme/github-buttons on GitHub" href="https://github.com/Balluff-BVS/halconscripts/raw/master/Filters/Smoothing/SmoothImage/smooth_image.zip" data-icon="octicon-cloud-download">Download</a></p>


SMOOTH IMAGE
==========

## Example

Original Picture             | Filtered Picture
:-------------------------:|:-------------------------:
![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Filters/Smoothing/SmoothImage/original.png?raw=true)  |  ![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Filters/Smoothing/SmoothImage/smooth_image.png?raw=true)

Description
----------

Smooths gray images using recursive filters originally developed by Deriche and Shen and using the non-recursive Gaussian filter. The following filters can be choosen via the parameter *Filter*.

Input Parameters
----------

**Filter** - Filter type

*Default value:* 'deriche2'

*List of values:* 'deriche1', 'deriche2', 'gauss', 'shen'

**Alpha** - Filter parameter: small values cause strong smoothing (vice versa by using bei 'gauss').

*Default value:* 0.5

*Suggested values:* 0.1, 0.2, 0.3, 0.5, 1.0, 1.5, 2.0, 2.5, 3.0, 4.0, 5.0, 7.0, 10.0

*Restriction:* 0 < Alpha
