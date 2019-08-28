# <p align="right"><a class="github-button" aria-label="Download ntkme/github-buttons on GitHub" href="https://github.com/Balluff-BVS/TestScripts/raw/master/Filters/Smoothing/Eliminate/EliminateMinMax/eliminate_min_max.zip" data-icon="octicon-cloud-download">Download</a></p>


ELIMINATE MIN MAX
==========

## Example

Original Picture             | Filtered Picture
:-------------------------:|:-------------------------:
![Image error](https://github.com/Balluff-BVS/TestScripts/blob/master/Filters/Smoothing/Eliminate/EliminateMinMax/gauss_distribiution.png?raw=true)  |  ![Image error](https://github.com/Balluff-BVS/TestScripts/blob/master/Filters/Smoothing/Eliminate/EliminateMinMax/eliminate_min_max.png?raw=true)

Description
----------

Smooths an image by replacing gray values with neighboring mean values, or local minima/maxima, to supress noise

Input Parameters
----------

**MaskWidth** - Width of filter mask.

*Default value:* 3

*Suggested values:*  3, 5, 7, 9

*Restriction:* value is odd

**MaskHeight** - Height of filter mask.

*Default value:* 3

*Suggested values:* 3, 5, 7, 9

*Restriction:* value is odd

**Gap** - Gap between local maximum/minimum and all other gray values of the neighborhood.

*Default value:* 1

*Suggested values:* 1.0, 2.0, 5.0, 10.0

**Mode** - Replacement rule (1 = next minimum/maximum, 2 = average, 3 =median).

*Default value:* 3

*List of values:* 1.0, 2.0, 5.0, 10.0
