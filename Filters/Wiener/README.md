# <p align="right"><a class="github-button" aria-label="Download ntkme/github-buttons on GitHub" href="https://github.com/Balluff-BVS/halconscripts/raw/master/Filters/Wiener/wiener_filter.zip" data-icon="octicon-cloud-download">Download</a></p>


WIENER FILTER
==========

## Example

Original Picture             | Filtered Picture
:-------------------------:|:-------------------------:
![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Filters/Wiener/original.png?raw=true)  |  ![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Filters/Wiener/wiener.png?raw=true)

Description
----------

Produces an estimate of the original image (= image without noise and blurring) by minimizing the mean square error between estimated and original image. Can be used to restore images corrupted by noise and/or blurring (e.g. motion blur, atmospheric turbulence or out-of-focus blur).

Input Parameters
----------

**Blurring** - Degree of motion-blur.

*Default value:* 

*Suggested values:*  5.0, 10.0, 20.0, 30.0, 40.0

**Angle** - Angle between direction of motion and x-axis (anticlockwise).

*Default value:* 0

*Suggested values:* 0, 45, 90, 180, 270

**Type** - PSF prototype resp. type of motion.

*Default value:* 3

*Suggested values:* 1, 2, 3, 4, 5

**MaskType** - Filter mask type.

*Default value:* 'circle'

*List of values:* 'circle', 'square'

**Radius** - Radius of the filter mask.

*Default value:* 1

*Suggested values:* 1, 2, 3, 4, 5, 6, 7, 8, 9, 11, 15, 19, 25, 31, 39, 47, 59

**Margin** - Border treatment.

*Default value:* 'mirrored'

*List of values:* 'mirrored', 'cyclic', 'continued', 0, 30, 60, 90, 120, 150, 180, 210, 240, 255
