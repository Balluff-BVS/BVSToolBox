# <p align="right"><a class="github-button" aria-label="Download ntkme/github-buttons on GitHub" href="https://github.com/Balluff-BVS/halconscripts/raw/master/Blob/DynamicThreshold/dynamic_threshold.zip" data-icon="octicon-cloud-download">Download</a></p>

DYNAMIC THRESHOLD
===========
Example
---------

Original Picture             | Thresholded Picture
:-------------------------:|:-------------------------:
![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Blob/DynamicThreshold/original.png?raw=true)  |  ![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Blob/DynamicThreshold/dynamic_threshold.png?raw=true)

Description
----------

Selects from the input image those regions in which the pixels fulfill a threshold condition.

The larger the mask size is chosen, the larger the found regions become. As a rule of thumb, the mask size should be about twice the diameter of the objects to be extracted. It is important not to set the parameter *Offset* to zero because in this case too many small regions will be found (noise). Values between 5 and 40 are a useful choice. The larger *Offset* is chosen, the smaller the extracted regions become.

Input parameters
----------

**MeanFilter_MaskWidth** - Width of filter mask.

*Default:* 59

*Suggested values:* 3, 5, 7, 9, 11, 15, 23, 31, 43, 61, 101

**MeanFilter_MaskHeight** - Height of filter mask.

*Default:* 59

*Suggested of values:* 3, 5, 7, 9, 11, 15, 23, 31, 43, 61, 101

**DynThreshold_Offset** - Offset applied to Threshold Image.

*Default:* 5

*Suggested values:* 1.0, 3.0, 5.0, 7.0, 10.0, 20.0, 30.0

**DynThreshold_LightDark** - Extract light, dark or similar areas?

*Default:* 'light'

*List of values:* 'dark', 'equal', 'light', 'not_equal'

**ClosingCircle_Radius** - Radius of the circular structuring element.

*Default:* 14.5

*Suggested values:* 1.5, 2.5, 3.5, 4.5, 5.5, 7.5, 9.5, 12.5, 15.5, 19.5, 25.5, 33.5, 45.5, 60.5, 110.5

Output
--------

A collection of regions.

Each of them may be used in further image processing ex. shape measurement.
