# <p align="right"><a class="github-button" aria-label="Download ntkme/github-buttons on GitHub" href="https://github.com/Balluff-BVS/TestScripts/raw/master/Filters/Smoothing/FillInterlace/fill_interlace.zip" data-icon="octicon-cloud-download">Download</a></p>


FILL INTERLACE
==========

## Example

Original Picture             | Filtered Picture
:-------------------------:|:-------------------------:
![Image error](https://github.com/Balluff-BVS/TestScripts/blob/master/Filters/Smoothing/FillInterlace/original.png?raw=true)  |  ![Image error](https://github.com/Balluff-BVS/TestScripts/blob/master/Filters/Smoothing/FillInterlace/fill_interlace.png?raw=true)

Description
----------
The operator fill_interlace calculates an interpolated full image or removes odd/even lines from a video image composed of two half images. If an image is recorded with a video camera it consists of two half images recorded at different times but stored in one image in the digital form. This can lead to several errors in further processing. In order to reduce these errors the video image is modified. Every second line is re-calculated or removed.

Input Parameters
----------

**Mode** - Instruction whether even or odd lines should be replaced/removed.

*Default value:* 'odd'

*List of values:* 'even', 'odd', 'rmeven', 'rmodd', 'switch'

