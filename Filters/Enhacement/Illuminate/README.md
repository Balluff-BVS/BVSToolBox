# <p align="right"><a class="github-button" aria-label="Download ntkme/github-buttons on GitHub" href="https://github.com/Balluff-BVS/halconscripts/raw/master/Filters/Enhacement/enhancement_filters.zip" data-icon="octicon-cloud-download">Download</a></p>

ILLUMINATE
==========

## Example

Original Picture             | Filtered Picture
:-------------------------:|:-------------------------:
![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Filters/Enhacement/Illuminate/original.png?raw=true)  |  ![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Filters/Enhacement/Illuminate/illuminate.png?raw=true)

Description
----------

Enhances contrast. Very dark parts of the image are “illuminated” more strongly, very light ones are “darkened”. If orig is the original gray value and mean is the corresponding gray value of the low pass filtered image detected via the operators mean_image and filter size *MaskHeight* x *MaskWidth*. 

Input Parameters
----------

**MaskWidth** - Width of low pass mask.

*Default value:* 101

*Suggested values:* 31, 41, 51, 71, 101, 121, 151, 201

**MaskHeight** - Height of low pass mask.

 *Default value:* 101
 
*Suggested values:* 31, 41, 51, 71, 101, 121, 151, 201

**Factor** - Scales the “correction gray value” added to the original gray values.

 *Default value:* 0.7
 
*Suggested values:* 0.3, 0.5, 0.7, 1.0, 1.5, 2.0, 3.0, 5.0

**Restriction:* 0 < Factor < 5

.
