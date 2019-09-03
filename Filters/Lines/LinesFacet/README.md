# <p align="right"><a class="github-button" aria-label="Download ntkme/github-buttons on GitHub" href="https://github.com/Balluff-BVS/halconscripts/raw/master/Filters/Lines/LinesFacet/lines_facet.zip" data-icon="octicon-cloud-download">Download</a></p>

LINES FACET
==============

## Example

Original Picture             | Extracted Lines
:-------------------------:|:-------------------------:
![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Filters/Lines/LinesFacet/original.png?raw=true)  |  ![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Filters/Lines/LinesFacet/lines_facet.png?raw=true)

Description
------------

Extracts lines from the image using the facet model, i.e., a least squares fit, to determine the parameters of a quadratic polynomial in x and y for each point of the image.

The parameter *MaskSize* determines the size of the window used for the least squares fit. Larger values of *MaskSize* lead to a larger smoothing of the image, but can lead to worse localization of the line. The parameters of the polynomial are used to calculate the line direction for each pixel.

Input parameters
----------------

**MaskSize** - Size of the facet model mask.

*Default:* 5

*Suggested values:* 3, 5, 7, 9, 11

**Low** - Lower threshold for the hysteresis threshold operation.

*Default:* 3

*Suggested values:* 0, 0.5, 1, 2, 3, 4, 5, 8, 10

*Restriction:* Low >= 0

**High** - Upper threshold for the hysteresis threshold operation.

*Default:* 8

*Suggested values:* 0, 0.5, 1, 2, 3, 4, 5, 8, 10, 12, 15, 18, 20, 25

**LightDark** - Extract bright or dark lines.

*Default:* 'light'

*List of values:* 'light', 'dark'

Output
----------

Contours of detected lines.
