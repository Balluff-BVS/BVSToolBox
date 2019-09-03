# <p align="right"><a class="github-button" aria-label="Download ntkme/github-buttons on GitHub" href="https://github.com/Balluff-BVS/halconscripts/raw/master/Filters/Smoothing/BinomialFilter/binomial_filter.zip" data-icon="octicon-cloud-download">Download</a></p>


BINOMIAL FILTER
==========

## Example

Original Picture             | Filtered Picture
:-------------------------:|:-------------------------:
![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Filters/Smoothing/BinomialFilter/original.png?raw=true)  |  ![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Filters/Smoothing/BinomialFilter/binomial_filter.png?raw=true)

Description
----------

Smooths the image Image using a binomial filter with a mask size of *MaskWidth* x *MaskHeight*

Input Parameters
----------

**MaskWidth** - Width of filter mask.

*Default value:* 5

*Suggested values:*  1, 3, 5, 7, 9, 11, 13, 15, 17, 19, 21, 23, 25, 27, 29, 31, 33, 35, 37

*Restriction:* value is odd

**MaskHeight** - Height of filter mask.

*Default value:* 5

*Suggested values:* 1, 3, 5, 7, 9, 11, 13, 15, 17, 19, 21, 23, 25, 27, 29, 31, 33, 35, 37

*Restriction:* value is odd
