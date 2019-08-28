# <p align="right"><a class="github-button" aria-label="Download ntkme/github-buttons on GitHub" href="https://github.com/Balluff-BVS/TestScripts/raw/master/Filters/Smoothing/Mean/MeanSp/mean_sp.zip" data-icon="octicon-cloud-download">Download</a></p>


MEAN SP
==========

## Example

Original Picture             | Filtered Picture
:-------------------------:|:-------------------------:
![Image error](https://github.com/Balluff-BVS/TestScripts/blob/master/Filters/Smoothing/Mean/MeanSp/sp_distribiution.png?raw=true)  |  ![Image error](https://github.com/Balluff-BVS/TestScripts/blob/master/Filters/Smoothing/Mean/MeanSp/mean_sp.png?raw=true)

Description
----------

Suppress salt and pepper noise.

The operator mean_sp carries out a smoothing by averaging the values. Only the gray values within the interval from MinThresh to MaxThresh are averaged. Gray values which are too light or too dark are ignored during summation. If no gray value lies within the default interval during summation the original gray value is adopted.

Input Parameters
----------

**MaskWidth** - Width of filter mask.

*Default value:* 3

*Suggested values:* 3, 5, 7, 9, 11

*Restriction:* odd value

**MaskHeight** - Height of filter mask.

*Default value:* 3

*Suggested values:* 3, 5, 7, 9

*Restriction:* odd value

**MinThresh** - Minimum gray value.

*Default value:* 1

*Suggested values:* 1, 5, 7, 9, 11, 15, 23, 31, 43, 61, 101

**MaxThresh** - Maximum gray value.

*Default value:* 254

*Suggested values:* 5, 7, 9, 11, 15, 23, 31, 43, 61, 101, 200, 230, 250, 254

*Restriction:* MinThresh <= MaxThresh

