# <p align="right"><a class="github-button" aria-label="Download ntkme/github-buttons on GitHub" href="https://github.com/Balluff-BVS/halconscripts/raw/master/Filters/Points/points_filters.zip" data-icon="octicon-cloud-download">Download</a></p>


CORNER RESPONSE
==========

## Example

Original Picture             | Filtered Picture
:-------------------------:|:-------------------------:
![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Filters/Points/CornerResponse/original.png?raw=true)  |  ![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Filters/Points/CornerResponse/corner_response.png?raw=true)

Description
----------

The *corner_response* extracts gray value corners in an image.

Input Parameters
----------

**Size** - Desired filtersize of the graymask.

*Default value:* 3 

*Suggested values:* 3, 5, 7, 9, 11

**Weight** - Weighting.

*Default value:* 0.04

*Range of values:* 0.0 <= Weight <= 0.3

