# <p align="right"><a class="github-button" aria-label="Download ntkme/github-buttons on GitHub" href="https://github.com/Balluff-BVS/TestScripts/raw/master/Filters/Smoothing/SigmaImage/sigma_image.zip" data-icon="octicon-cloud-download">Download</a></p>


SIGMA IMAGE
==========

## Example

Original Picture             | Filtered Picture
:-------------------------:|:-------------------------:
![Image error](https://github.com/Balluff-BVS/TestScripts/blob/master/Filters/Smoothing/SigmaImage/original.png?raw=true)  |  ![Image error](https://github.com/Balluff-BVS/TestScripts/blob/master/Filters/Smoothing/SigmaImage/sigma_image.png?raw=true)

Description
----------

The operator sigma_image carries out a non-linear smoothing of the gray values of all input images. All pixels in a rectangular window are used to determine the new gray value of the central pixel of this window. First, the gray value standard deviation of all pixels in the window is calculated. Then, all pixels of the window with a gray value that differs from the gray value of the central pixel by less than Sigma times this standard deviation are used to calculate the new gray value of the central pixel. The gray value of the central pixel is the average of the gray values of the selected pixels. If no pixel could be selected for the averaging of the gray values, the gray value of the central pixel remains unchanged.

Input Parameters
----------

**MaskHeight** - Height of the mask (number of lines).

*Default value:* 5

*Suggested values:* 3, 5, 7, 9, 11, 13, 15

*Restriction:* value is odd

**MaskWidth** - Width of the mask (number of columns).

*Default value:* 5

*Suggested values:* 3, 5, 7, 9, 11, 13, 15

*Restriction:* value is odd

**Sigma** - Max. deviation to the average.

*Default value:* 3

*Suggested values:* 3, 5, 7, 9, 11, 20, 30, 50


