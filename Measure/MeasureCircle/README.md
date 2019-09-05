# <p align="right"><a class="github-button" aria-label="Download ntkme/github-buttons on GitHub" href="https://github.com/Balluff-BVS/halconscripts/raw/master/Measure/MeasureCircle/measure_circle.zip" data-icon="octicon-cloud-download">Download</a></p>

MEASURE CIRCLE
=================

Example
--------

<p align="center">
  <img src="https://github.com/Balluff-BVS/halconscripts/blob/master/Measure/MeasureCircle/measure_circle.png?raw=true" alt="Picture error">
</p>

Description
-------------

Function fits circular contour into given input region and returns its features such as center coordinates and radius.

Input parameters
----------------

**object_to_measure** - regions obtained ex. by CheckBlobs which is searched for cirlces to measure

**measure_length1** - Half length of the measure regions perpendicular to the boundary.

*Default:* 20.0

*List of values:* 10.0, 20.0, 30.0

**measure_length2** - Half length of the measure regions tangetial to the boundary.

*Default:* 5.0

*Suggested values:* 3.0, 5.0, 10.0

**measure_distance** - Specifies the desired distance between the centers of two measure regions.

*Default:* 10.0

*Suggested values:* 5.0, 15.0, 20.0, 30.0

**measure_sigma** - Sigma of the Gaussian function for the smoothing.

*Default:* 1.0

*Suggested values:* 0.4, 0.6, 0.8, 1.0, 1.5, 2.0, 3.0, 4.0, 5.0, 7.0, 10.0

**measure_threshold** - Minimum edge amplitude.

*Default:* 30.0

*Suggested values:* 5.0, 10.0, 20.0, 30.0, 40.0, 50.0, 60.0, 70.0, 90.0, 110.0

**measure_transition** - Specifies the use of dark/light or light/dark edges.

*Default:* 'all'

*List of values:* 'all', 'negative', 'positive', 'uniform'

**min_score** - Determines what score a potential instance must at least have to be regarded as a valid instance of the metrology object.

*Default:* 0.7

*Suggested values:* 0.5, 0.7, 0.9

**num_instances** - Specifies the maximum number of successfully fitted instances of each metrology object after which the fitting will stop

*Default:* 1

*Suggested values:* 1, 2, 3, 4

**distance_threshold** - An edge point is considered to be part of a fitted geometric shape, if the distance of the edge point to the geometric shape does not exceed the value of 'distance_threshold'.

*Default:* 3.5

*Suggested values:* 0, 1.0, 2.0, 3.5, 5.0

**max_num_iterations** - Defines upper limit for the computed number of iterations

*Default:* -1

*Suggested values:* 10, 100, 1000

**instances_outside_measure_regions** - If the value of the parameter 			'instances_outside_measure_regions' is set to the value 'false', only resulting instances of an metrology object are valid that are inside the major axis of the measure regions of this metrology object.

*Default:* 'false'

*Suggested values:* 'false', 'true'

**circle_to_measure** - index of circle which parameters are displayed

Output
-----------

Contour of the measured circle.

Rectangular contours used to measure the region.

**measure_circle.hdev** returns red pointer showing circle which parameters are currently returned as output. User may switch between regions by changing *circle_to_measure* parameter. It returns all possible parameters of one of measured regions only.

**measure_circle_return_array.hdev** returns arrays with all possible parameters of all measured regions.

Measured parameters:

**center_y, center_x** - coordinates of the center of circle

**radius** - orientation of the major axis

**number_of_circles** - how many circles are fitted in the input region
