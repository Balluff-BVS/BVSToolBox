# <p align="right"><a class="github-button" aria-label="Download ntkme/github-buttons on GitHub" href="https://github.com/Balluff-BVS/TestScripts/raw/master/Filters/Smoothing/Median/median_filters.zip" data-icon="octicon-cloud-download">Download</a></p>


MEDIAN RECT
==========

## Example

Original Picture             | Filtered Picture
:-------------------------:|:-------------------------:
![Image error](https://github.com/Balluff-BVS/TestScripts/blob/master/Filters/Smoothing/Median/MedianRect/original.png?raw=true)  |  ![Image error](https://github.com/Balluff-BVS/TestScripts/blob/master/Filters/Smoothing/Median/MedianRect/median_rect.png?raw=true)

Description
----------

Performs a median filter on the input image Image with a rectangular mask of size *MaskWidth* × *MaskHeight*.

Conceptually, the median filter sorts all gray values within the mask in ascending order and then selects the median of the gray values. The median is the “middle” one of the sorted gray values, i.e., the gray value with rank (position) (MaskWidth * MaskHeight - 1) / 2 + 1 of the sorted gray values, where the rank 1 corresponds to the smallest gray value and the rank MaskWidth * MaskHeight corresponds to the largest gray value within the mask

Input Parameters
----------

**MaskWidth** - Width of the filter mask.

*Default value:* 15

*Suggested values:* 3, 5, 7, 9, 11, 13, 15, 17, 19, 21, 31, 49, 51, 61, 71, 81, 91, 101

**MaskHeight** - Height of the filter mask.

*Default value:* 15

*Suggested values:* 3, 5, 7, 9, 11, 13, 15, 17, 19, 21, 31, 49, 51, 61, 71, 81, 91, 101
