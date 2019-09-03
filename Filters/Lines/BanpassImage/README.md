# <p align="right"><a class="github-button" aria-label="Download ntkme/github-buttons on GitHub" href="https://github.com/Balluff-BVS/halconscripts/raw/master/Filters/Lines/BanpassImage/bandpass_image.zip" data-icon="octicon-cloud-download">Download</a></p>

BANDPASS IMAGE
==============

## Example

Original Picture             | Extracted Lines
:-------------------------:|:-------------------------:
![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Filters/Lines/BanpassImage/original.png?raw=true)  |  ![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Filters/Lines/BanpassImage/bandpass_image.png?raw=true)

Description
------------

Extracts lines from the image using bandpass filter.

All contours having at least *Length* points are returned. Since contours are split at junction points, possibly long contours may be split into several short segments because of short adjacent lines, even if they are longer than *Length* points, if *Mode = 'filter'* was selected. This can be avoided by setting *Mode = 'generalize1'*. In this case, the contours are generated as if the segments shorter than *Length* were not contained in the input region. In order to preserve line segments, which are split into very short segments by the crossing of short lines, *Mode = 'generalize2'* can be selected. In this case, line segments are preserved if they end in two junction points, even if they are shorter than *Length*.

Input parameters
----------------

**MinGray** - mininum threshold value

*Default:* 0

*Range of values:* 0 <= MinGray <= 255

*Restriction:* MinGray < MaxGray

**MaxGray** - maximum threshold value

*Default:* 255

*Range of values:* 0 <= MaxGray <= 255

*Restriction:* MaxGray > MinGray

**Length** - Minimum number of points a contour has to have.

*Default:* 1

*Suggested values:* 1, 2, 3, 5, 10, 20

**Mode** - Contour filter mode.

*Default:* 'filter'

*List of values:* 'filter', 'generalize1', 'generalize2'

Output
----------

Contours of detected lines.
