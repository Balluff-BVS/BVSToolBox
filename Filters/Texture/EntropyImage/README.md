# <p align="right"><a class="github-button" aria-label="Download ntkme/github-buttons on GitHub" href="https://github.com/Balluff-BVS/TestScripts/raw/master/Filters/Texture/texture_filters.zip" data-icon="octicon-cloud-download">Download</a></p>


ENTROPY IMAGE
==========

## Example

Original Picture             | Filtered Picture
:-------------------------:|:-------------------------:
![Image error](https://github.com/Balluff-BVS/TestScripts/blob/master/Filters/Texture/EntropyImage/original.png?raw=true)  |  ![Image error](https://github.com/Balluff-BVS/TestScripts/blob/master/Filters/Texture/EntropyImage/entropy_image.png?raw=true)

Description
----------

Calculate the entropy of gray values within a rectangular window.

Input Parameters
----------

**Width, Height** - width/height of the mask in which the standard deviation is calculated

*Default value:* 11

*Suggested values:* 3, 5, 7, 9, 11, 13, 15, 17, 19, 21, 23, 25

*Restriction:* 3 <= Width, Height (both values are odd)
