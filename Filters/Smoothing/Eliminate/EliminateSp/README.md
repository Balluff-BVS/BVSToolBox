# <p align="right"><a class="github-button" aria-label="Download ntkme/github-buttons on GitHub" href="https://github.com/Balluff-BVS/halconscripts/raw/master/Filters/Smoothing/Eliminate/EliminateSp/eliminate_sp.zip" data-icon="octicon-cloud-download">Download</a></p>


ELIMINATE SP
==========

## Example

Original Picture             | Filtered Picture
:-------------------------:|:-------------------------:
![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Filters/Smoothing/Eliminate/EliminateSp/sp_distribiution.png?raw=true)  |  ![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Filters/Smoothing/Eliminate/EliminateSp/eliminate_sp.png?raw=true)

Description
----------

Replace values outside of thresholds with average value.

Input Parameters
----------

**MaskWidth** - Width of filter mask.

*Default value:* 3

*Suggested values:*  3, 5, 7, 9, 11

*Restriction:* value is odd

**MaskHeight** - Height of filter mask.

*Default value:* 3

*Suggested values:* 3, 5, 7, 9, 11

*Restriction:* value is odd

**MinThresh** - Minimum gray value.

*Default value:* 1

*Suggested values:* 1, 5, 7, 9, 11, 15, 23, 31, 43, 61, 101

**MaxThresh** - Maximum gray value.

*Default value:* 3

*Suggested of values:* 5, 7, 9, 11, 15, 23, 31, 43, 61, 101, 200, 230, 250, 254

*Restriction:* MinThresh <= MaxThresh
