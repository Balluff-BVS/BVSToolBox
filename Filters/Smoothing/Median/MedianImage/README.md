# <p align="right"><a class="github-button" aria-label="Download ntkme/github-buttons on GitHub" href="https://github.com/Balluff-BVS/halconscripts/raw/master/Filters/Smoothing/Median/median_filters.zip" data-icon="octicon-cloud-download">Download</a></p>


MEDIAN IMAGE
==========

## Example

Original Picture             | Filtered Picture
:-------------------------:|:-------------------------:
![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Filters/Smoothing/Median/MedianImage/original.png?raw=true)  |  ![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Filters/Smoothing/Median/MedianImage/median_image.png?raw=true)

Description
----------

Performs a median filter on the input image with a square or circular mask and returns the filtered image.

Conceptually, the median filter sorts all gray values within the mask in ascending order and then selects the median of the gray values. The median is the “middle” one of the sorted gray values, i.e., the gray value with rank (position) (N - 1) / 2 + 1 of the sorted gray values, where N denotes the number of pixels covered by the filter mask. Here, the rank 1 corresponds to the smallest gray value and the rank N corresponds to the largest gray value within the mask.

Input Parameters
----------

**MaskType** - Filter mask type.

*Default value:* 'circle'

*List of values:* 'circle', 'square'

**Radius** - Radius of the filter mask.

*Default value:* 1

*Suggested values:* 1, 2, 3, 4, 5, 6, 7, 8, 9, 11, 15, 19, 25, 31, 39, 47, 59

**Margin** - Border treatment.

*Default value:* 'mirrored'

*Suggested values:* 'mirrored', 'cyclic', 'continued', 0, 30, 60, 90, 120, 150, 180, 210, 240, 255
