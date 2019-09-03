# <p align="right"><a class="github-button" aria-label="Download ntkme/github-buttons on GitHub" href="https://github.com/Balluff-BVS/halconscripts/raw/master/Filters/Enhacement/enhancement_filters.zip" data-icon="octicon-cloud-download">Download</a></p>

EMPHASIZE
==========

## Example

Original Picture             | Filtered Picture
:-------------------------:|:-------------------------:
![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Filters/Enhacement/Emphasize/original.png?raw=true)  |  ![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Filters/Enhacement/Emphasize/emphasize.png?raw=true)

Description
----------

Emphasizes high frequency areas of the image (edges and corners). The resulting images appears sharper.

Input Parameters
----------

**MaskWidth** - Width of low pass mask.

*Default value:* 7

*Suggested values:* 3, 5, 7, 9, 11, 15, 21, 25, 31, 39

*Restriction:* 3 <= MaskWidth <= 201

**MaskHeight** - Height of the low pass mask.

 *Default value:* 7
 
*Suggested values:* 3, 5, 7, 9, 11, 15, 21, 25, 31, 39

*Restriction:* 3 <= MaskHeight <= 201

**Factor** - Intensity of contrast emphasis.

 *Default value:* 1.0
 
*Suggested values:* 0.3, 0.5, 0.7, 1.0, 1.4, 1.8, 2.0

**Restriction:* 0 < Factor < 20
