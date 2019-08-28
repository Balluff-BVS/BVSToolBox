# <p align="right"><a class="github-button" aria-label="Download ntkme/github-buttons on GitHub" href="https://github.com/Balluff-BVS/halconscripts/raw/master/Filters/Smoothing/Rank/RankImage/rank_image.zip" data-icon="octicon-cloud-download">Download</a></p>


RANK IMAGE
==========

## Example

Original Picture             | Filtered Picture
:-------------------------:|:-------------------------:
![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Filters/Smoothing/Rank/RankImage/original.png?raw=true)  |  ![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Filters/Smoothing/Rank/RankImage/rank_image.png?raw=true)

Description
----------

Compute a rank filter with arbitrary masks.

Conceptually, the rank filter sorts all gray values within the mask in ascending order and then selects the gray value with rank Rank. The rank 1 corresponds to the smallest gray value. rank_image can be used, for example, to suppress noise or to suppress unwanted objects that are smaller than the mask.

Input Parameters
----------

**Rank** - Rank of the output gray value.

*Default value:* 5

*Suggested values:* 3, 5, 7, 9, 11, 13, 15, 17, 19, 21, 31, 49, 51, 61, 71, 81, 91, 101

**Margin** - Border treatment.

*Default value:* 'mirrored'

*Suggested values:* 'mirrored', 'cyclic', 'continued', 0, 30, 60, 90, 120, 150, 180, 210, 240, 255
