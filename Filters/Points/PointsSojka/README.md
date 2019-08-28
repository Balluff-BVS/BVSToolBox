# <p align="right"><a class="github-button" aria-label="Download ntkme/github-buttons on GitHub" href="https://github.com/Balluff-BVS/halconscripts/raw/master/Filters/Points/points_filters.zip" data-icon="octicon-cloud-download">Download</a></p>


POINTS SOJKA
==========

## Example

Original Picture             | Filtered Picture
:-------------------------:|:-------------------------:
![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Filters/Points/PointsSojka/original.png?raw=true)  |  ![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Filters/Points/PointsSojka/points_sojka.png?raw=true)

Description
----------

Defines a corner as the point of intersection of two straight, non-collinear gray value edges. To decide whether a point of the input image is a corner or not, a neighborhood of *MaskSize* x *MaskSize* points is inspected. Only those image regions that are relevant for the decision are considered. Pixels with a magnitude of the gradient of less than *MinGrad* are ignored from the outset.

Input Parameters
----------

**SigmaW** - Sigma of the weight function according to the distance to the corner candidate.

*Default value:* 2.5

*Suggested values:* 2.0, 2.2, 2.4, 2.5, 2.6, 2.8, 3.0

**SigmaD** - Sigma of the weight function for the distance to the ideal gray value edge.

*Default value:* 0.75

*Suggested values:* 0.6, 0.7, 0.75, 0.8, 0.9, 1.0

*Restriction:* 0.6 <= SigmaD <= 1.0

**MinGrad** - Threshold for the magnitude of the gradient.

*Default value:* 30

*Suggested values:* 20.0, 15.0, 30.0, 35.0, 40.0

**MinApparentness** - Threshold for Apparentness.

*Default value:* 90

*Suggested values:* 30.0, 60.0, 90.0, 150.0, 300.0, 600.0, 1500.0

**MinAngle** - Threshold for the direction change in a corner point (radians).

*Default value:* 0.5

*Restriction:* 0.0 <= MinAngle <= pi

**Subpix** - Subpixel precise calculation of the corner points.

*Default value:*  'false'

*Suggested values:*  'false',  'true'



