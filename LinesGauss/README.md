# <p align="right"><a class="github-button" aria-label="Download ntkme/github-buttons on GitHub" href="https://github.com/Balluff-BVS/TestScripts/raw/master/LinesGauss/lines_gauss.zip" data-icon="octicon-cloud-download">Download</a></p>

LINES GAUSS
==============

## Example

Original Picture             | Extracted Lines
:-------------------------:|:-------------------------:
![Image error](https://github.com/Balluff-BVS/TestScripts/blob/master/LinesGauss/original.png?raw=true)  |  ![Image error](https://github.com/Balluff-BVS/TestScripts/blob/master/LinesGauss/lines_gauss.png?raw=true)

Description
------------

Extracts lines from the image, given their maximal width and contrast from the background.

Later enables processing the set of found lines, by segmenting them, uniting into longer ones and selecting lines in given range of length.

Input parameters
----------------

**max_line_width** - maximal width of lines to be detected

*Default:* 8

**contrast** - contrast between lines to detect and background

*Default:* 12

**light_dark** - extract bright or dark lines

*Default:* 'light'

*List of values:* 'dark', 'light'

**extract_width** - should the line width be extracted?

*Default:* 'true'

*List of values:* 'false', 'true'

**line_model** - line model used to correct the line position and width

*Default:* 'bar-shaped'

*List of values:* 'bar-shaped', 'gaussian', 'none', 'parabolic'

**complete_juntions** - should junctions be added where they cannot be extracted?

*Default:* 'true'

*List of values:* 'false', 'true'

After detecting lines, they are processed by segmenting and then by uniting collinear segments. Later, contours in the given range of values are selected.

**SegmentContour_smoothCont** - number of points used for smoothing the contours.

*Default:* 5

*Suggested values:* 0, 3, 5, 7, 9

**SegmentContour_MaxLineDist1, SegmentContour_MaxLineDist2** - maximum distance between a contour and the approximating line. Segmenting is performed in 2 iterations: firstly using MaxLineDist1, secondly using value of MaxLineDist2, if MaxLineDist2 < MaxLineDist1

*Default:* MaxLineDist1 = 4.0, MaxLineDist2 = 2.0

*Suggested values:* 1.0, 1.5, 2.0, 2.5, 3.0, 3.5

**UnionContours_MaxDistAbs** - maximum length of the gap between two contours, measured along the regression line of the reference contour

*Default:* 10.0

*Restriction:* 0.0 <=UnionContours_MaxDistAbs

**UnionContours_MaxDistRel** - maximum length of the gap between two contours, relative to the length of the reference contour, both measured along the regression line of the reference contour

*Default:* 1.0

*Restriction:* 0.0 <= UnionContours_MaxDistRel

**UnionContours_MaxShift** - maximum distance of the second contour from the regression line of the reference contour

*Default:* 2.0

*Restriction:* 0.0 <= UnionContours_MaxShift

**UnionContours_MaxAngle** - maximum angle between the regression lines of two contours

*Default:* 0.1

*Suggested values:* 0.0 <= UnionContours_MaxAngle <= 0.785

**SelectContours_MinLength, SelectContours_MaxLength** - all contours whose length is smaller than MinLength or larger than MaxLength are not returned.

*Default:* MinLength = 0.5, MaxLength = 200

Output
----------

A set of detected lines after process of segmenting, uniting and selecting (in contour format).

**number_of_lines_found** - how many lines are detected.
