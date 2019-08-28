# <p align="right"><a class="github-button" aria-label="Download ntkme/github-buttons on GitHub" href="https://github.com/Balluff-BVS/TestScripts/raw/master/Filters/Smoothing/Median/median_filters.zip" data-icon="octicon-cloud-download">Download</a></p>


MEDIAN SEPARATE
==========

## Example

Original Picture             | Filtered Picture
:-------------------------:|:-------------------------:
![Image error](https://github.com/Balluff-BVS/TestScripts/blob/master/Filters/Smoothing/Median/MedianSeparate/original.png?raw=true)  |  ![Image error](https://github.com/Balluff-BVS/TestScripts/blob/master/Filters/Smoothing/Median/MedianSeparate/median_separate.png?raw=true)

Description
----------

Separated median filtering with rectangle masks.

The operator median_separate carries out a variation of the median filtering: First two auxiliary images are created. The first one originates from a median filtering with a horizontal mask having a height of one pixel and the width MaskWidth followed by filtering with a vertical mask having the height MaskHeight and width of one pixel. The second auxiliary image is created by filtering with the same masks, but with a reversed sequence of the operation: first the vertical, then the horizontal mask. The output image results from averaging the two auxiliary images pixel by pixel.

Input Parameters
----------

**MaskWidth** - Width of the filter mask.

*Default value:* 25

*Suggested values:* 1, 3, 5, 7, 9, 11, 13, 15, 17, 19, 21, 27, 43, 51, 67, 91, 121, 151

**MaskHeight** - Height of the filter mask.

*Default value:* 25

*Suggested values:* 1, 3, 5, 7, 9, 11, 13, 15, 17, 19, 21, 27, 43, 51, 67, 91, 121, 151

**Margin** - Border treatment.

*Default value:* 'mirrored'

*Suggested values:* 'mirrored', 'cyclic', 'continued', 0, 30, 60, 90, 120, 150, 180, 210, 240, 255

