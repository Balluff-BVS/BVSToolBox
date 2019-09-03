# <p align="right"><a class="github-button" aria-label="Download ntkme/github-buttons on GitHub" href="https://github.com/Balluff-BVS/halconscripts/raw/master/Filters/Enhacement/enhancement_filters.zip" data-icon="octicon-cloud-download">Download</a></p>

EQU HISTO IMAGE
==========

## Example

Original Picture             | Filtered Picture
:-------------------------:|:-------------------------:
![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Filters/Enhacement/EquHistoImage/original.png?raw=true)  |  ![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Filters/Enhacement/EquHistoImage/equ_histo_image.png?raw=true)

Description
----------

The operator enhances the contrast. The starting point is the histogram of the input images.

Maxima in the original histogram are “spreaded” and thus the contrast in image regions with these frequently occurring gray values is increased. Supposedly homogeneous regions receive more easily visible structures. On the other hand, of course, the noise in the image increases correspondingly. Minima in the original histogram are dually “compressed”.
