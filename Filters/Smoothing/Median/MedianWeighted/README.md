# <p align="right"><a class="github-button" aria-label="Download ntkme/github-buttons on GitHub" href="https://github.com/Balluff-BVS/TestScripts/raw/master/Filters/Smoothing/Median/median_filters.zip" data-icon="octicon-cloud-download">Download</a></p>


MEDIAN WEIGHTED
==========

## Example

Original Picture             | Filtered Picture
:-------------------------:|:-------------------------:
![Image error](https://github.com/Balluff-BVS/TestScripts/blob/master/Filters/Smoothing/Median/MedianWeighted/original.png?raw=true)  |  ![Image error](https://github.com/Balluff-BVS/TestScripts/blob/master/Filters/Smoothing/Median/MedianWeighted/median_weighted.png?raw=true)

Description
----------

The operator median_weighted calculates the median of the gray values within a local environment. In contrast to median_image, which uses all gray values within the environment exactly once, the operator median_weighted weights all gray values several times depending on their position. A gray value is received into the field to be sorted several times according to its weighting.

Input Parameters
----------

**MaskType** - Type of median mask.

*Default value:* 'inner'

*List of values:* 'gauss', 'inner'
