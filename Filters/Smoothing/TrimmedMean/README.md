# <p align="right"><a class="github-button" aria-label="Download ntkme/github-buttons on GitHub" href="https://github.com/Balluff-BVS/halconscripts/raw/master/Filters/Smoothing/TrimmedMean/trimmed_mean.zip" data-icon="octicon-cloud-download">Download</a></p>


TRIMMED MEAN
==========

## Example

Original Picture             | Filtered Picture
:-------------------------:|:-------------------------:
![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Filters/Smoothing/TrimmedMean/original.png?raw=true)  |  ![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Filters/Smoothing/TrimmedMean/trimmed_mean.png?raw=true)

Description
----------

The operator trimmed_mean carries out a non-linear smoothing of the gray values of all input images. The filter mask (Mask) is passed in the form of a region. The average of *Number* gray values located near the median is calculated.

The indicated mask is put over the image to be filtered in such a way that the center of the mask touches all pixels once. For each of these pixels all neighboring pixels covered by the mask are sorted in an ascending sequence according to their gray values. Thus, each of these sorted gray value sequences contains exactly as many gray values as the mask has pixels.

Input Parameters
----------

**Number** - Number of averaged pixels. Typical value: Surface(Mask) / 2.

*Default value:* 5

*Suggested values:* 1, 3, 5, 7, 9, 11, 13, 15, 17, 19, 21, 23, 25, 27, 29, 31

**Margin** - Border treatment.

*Default value:* 'mirrored'

*Suggested values:* 'mirrored', 'cyclic', 'continued', 0, 30, 60, 90, 120, 150, 180, 210, 240, 255
