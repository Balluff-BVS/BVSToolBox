# <p align="right"><a class="github-button" aria-label="Download ntkme/github-buttons on GitHub" href="https://github.com/Balluff-BVS/TestScripts/raw/master/Filters/Smoothing/Rank/RankRect/rank_rect.zip" data-icon="octicon-cloud-download">Download</a></p>


RANK RECT
==========

## Example

Original Picture             | Filtered Picture
:-------------------------:|:-------------------------:
![Image error](https://github.com/Balluff-BVS/TestScripts/blob/master/Filters/Smoothing/Rank/RankRect/original.png?raw=true)  |  ![Image error](https://github.com/Balluff-BVS/TestScripts/blob/master/Filters/Smoothing/Rank/RankRect/rank_rect.png?raw=true)

Description
----------

Compute a rank filter with rectangular masks.

Conceptually, the rank filter sorts all gray values within the mask in ascending order and then selects the gray value with rank Rank. The rank 1 corresponds to the smallest gray value. rank_image can be used, for example, to suppress noise or to suppress unwanted objects that are smaller than the mask.

Input Parameters
----------

**MaskWidth** - Width of the filter mask.

*Default value:* 15

*Suggested values:* 3, 5, 7, 9, 11, 13, 15, 17, 19, 21, 31, 49, 51, 61, 71, 81, 91, 101

**MaskHeight** - Height of the filter mask.

*Default value:* 15

*Suggested values:* 3, 5, 7, 9, 11, 13, 15, 17, 19, 21, 31, 49, 51, 61, 71, 81, 91, 101

**Rank** - Rank of the output gray value.

*Default value:* 15

*Suggested values:* 3, 5, 7, 9, 11, 13, 15, 17, 19, 21, 31, 49, 51, 61, 71, 81, 91, 101
