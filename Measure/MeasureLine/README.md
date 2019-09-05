# <p align="right"><a class="github-button" aria-label="Download ntkme/github-buttons on GitHub" href="https://github.com/Balluff-BVS/halconscripts/raw/master/Measure/MeasureLine/measure_line.zip" data-icon="octicon-cloud-download">Download</a></p>

MEASURE LINE
=================

Example
--------

<p align="center">
  <img src="https://github.com/Balluff-BVS/halconscripts/blob/master/Measure/MeasureLine/measure_line.png?raw=true" alt="Picture error">
</p>

Description
-------------

Function fits linear, closed contour into given input region, then segments it into separate lines of given length and returns their features such as coordinates of beginning and end points and length.

Input parameters
----------------

**object_to_measure** - regions obtained ex. by CheckBlobs which contours to measure are generated

**line_to_measure** - index of line which parameters are displayed

**measure_length1** - Half length of the measure regions perpendicular to the boundary.

*Default:* 20.0

*List of values:* 10.0, 20.0, 30.0

**measure_length2** - Half length of the measure regions tangetial to the boundary.

*Default:* 5.0

*Suggested values:* 3.0, 5.0, 10.0

**measure_sigma** - Sigma of the Gaussian function for the smoothing.

*Default:* 1.0

*Suggested values:* 0.4, 0.6, 0.8, 1.0, 1.5, 2.0, 3.0, 4.0, 5.0, 7.0, 10.0

**measure_threshold** - Minimum edge amplitude.

*Default:* 30.0

*Suggested values:* 5.0, 10.0, 20.0, 30.0, 40.0, 50.0, 60.0, 70.0, 90.0, 110.0

User has to approximate the range of values for measured lines (**SelectContours**):

**SelectContours_MinLength, SelectContours_MaxLength** - all contours whose length is smaller than MinLength or larger than MaxLength are not returned. 

*Default:* MinLength = 0.5, MaxLength = 200

Closed contours are segmented into separate lines, which requires smoothing it and defining a deviation between input contour and approximating line (**SegmentContours**):

**SegmentContours_SmoothCont** - number of points used for smoothing the contours

*Default:* 5

*Suggested values:* 0, 3, 5, 7, 9 (SmoothCont is odd value)

**SegmentContours_MaxLineDist1, MaxLineDist2** - maximum distance between a contour and the approximating line. Segmenting is performed in 2 iterations: firstly using MaxLineDist1, secondly using value of MaxLineDist2, if MaxLineDist2 < MaxLineDist1

*Default:* MaxLineDist1 = 4.0, MaxLineDist2 = 2.0

*Suggested values:* 1.0, 1.5, 2.0, 2.5, 3.0, 3.5 

After segmentation, short but collinear lines are united into longer ones. To run the function, maximal linear and angular distance between lines has to be defined (**UnionContours**):

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


Output
-----------

Contour of the measured line.

Rectangular contours used to measure the line.

**measure_line.hdev** returns red pointer showing line which parameters are currently returned as output. User may switch between regions by changing *line_to_measure* parameter. It returns all possible parameters of one of measured regions only.

**measure_line_return_array.hdev** returns arrays with all possible parameters of all measured regions.

Measured parameters:

**x_begin, y_begin** - coordinates of the beginning point of line

**x_end, y_end** - coordinates of the ending point of line

**line_length** - distance between ending and beginning points

**number_of_lines** - how many lines are extracted from region to measure
