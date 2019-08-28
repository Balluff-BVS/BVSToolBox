# <p align="right"><a class="github-button" aria-label="Download ntkme/github-buttons on GitHub" href="https://github.com/Balluff-BVS/TestScripts/raw/master/Filters/Smoothing/Mean/MeanImage/mean_image.zip" data-icon="octicon-cloud-download">Download</a></p>


MEAN IMAGE
==========

## Example

Original Picture             | Filtered Picture
:-------------------------:|:-------------------------:
![Image error](https://github.com/Balluff-BVS/TestScripts/blob/master/Filters/Smoothing/Mean/MeanImage/original.png?raw=true)  |  ![Image error](https://github.com/Balluff-BVS/TestScripts/blob/master/Filters/Smoothing/Mean/MeanImage/mean_image.png?raw=true)

Description
----------

The operator mean_image carries out a linear smoothing with the gray values of all input images. The filter matrix consists of ones (evaluated equally) and has the size *MaskHeight* x *MaskWidth*.

Input Parameters
----------

**MaskWidth** - Width of filter mask.

*Default value:* 9

*Suggested values:* 3, 5, 7, 9, 11, 15, 23, 31, 43, 61, 101

*Restriction:* odd value

**MaskHeight** - Height of filter mask.

*Default value:* 9

*Suggested values:* 3, 5, 7, 9, 11, 15, 23, 31, 43, 61, 101

*Restriction:* odd value
