# <p align="right"><a class="github-button" aria-label="Download ntkme/github-buttons on GitHub" href="https://github.com/Balluff-BVS/halconscripts/raw/master/Filters/Points/points_filters.zip" data-icon="octicon-cloud-download">Download</a></p>


DOTS IMAGE
==========

## Example

Original Picture             | Filtered Picture
:-------------------------:|:-------------------------:
![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Filters/Points/DotsImage/original.png?raw=true)  |  ![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Filters/Points/DotsImage/dots_image.png?raw=true)

Description
----------

Enhances circular dots of diameter *Diameter* in the input image. Hence, *dots_image* is especially suited for the segmentation of dot prints, e.g., in OCR applications. The enhancement is performed by using matched filters with filter masks that are tuned for a particular dot size.

Input Parameters
----------

**Diameter** - Diameter of the dots to be enhanced.

*Default value:* 5

*List of values:* 3, 5, 7, 9, 11, 13, 15, 17, 19, 21, 23

**FilterType** - Enhance dark, light, or all dots.

*Default value:* 'light'

*List of values:* 'all', 'dark', 'light'

**PixelShift** - Shift of the filter response.

*Default value:* 0

*List of values:* -1, 0, 1, 2
