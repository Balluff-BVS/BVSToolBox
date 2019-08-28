# <p align="right"><a class="github-button" aria-label="Download ntkme/github-buttons on GitHub" href="https://github.com/Balluff-BVS/TestScripts/raw/master/Filters/Smoothing/MidrangeImage/midrange_image.zip" data-icon="octicon-cloud-download">Download</a></p>


MIDRANGE IMAGE
==========

## Example

Original Picture             | Filtered Picture
:-------------------------:|:-------------------------:
![Image error](https://github.com/Balluff-BVS/TestScripts/blob/master/Filters/Smoothing/MidrangeImage/original.png?raw=true)  |  ![Image error](https://github.com/Balluff-BVS/TestScripts/blob/master/Filters/Smoothing/MidrangeImage/midrange_image.png?raw=true)

Description
----------

Forms the average of maximum and minimum inside the indicated mask in the whole image. The indicated mask (= region of the mask image) is put over the image to be filtered in such a way that the center of the mask touches all pixels once.

Input Parameters
----------

**Margin** - Border treatment.

*Default value:*  'mirrored'

*Suggested values:*  'mirrored', 'cyclic', 'continued', 0, 30, 60, 90, 120, 150, 180, 210, 240, 255
