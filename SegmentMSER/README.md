# <p align="right"><a class="github-button" aria-label="Download ntkme/github-buttons on GitHub" href="https://github.com/Balluff-BVS/halconscripts/raw/master/SegmentMSER/segment_mser.zip" data-icon="octicon-cloud-download">Download</a></p>

SEGMENT MSER
===========
Example
---------
<p align="center">
  <img src="https://github.com/Balluff-BVS/halconscripts/raw/master/SegmentMSER/segment_mser.PNG">
</p>

Description
----------

Segments an image into regions of homogenous gray values using the approach of Maximally Stable Extremal Regions (MSER). The segmentation process determines if a region is homogenous by observing the local region surrounding. Therefore, the operator is particularly suited to robustly segment objects in front of inhomogeneous background or in applications with changing illumination. 

Input parameters
----------

**polarity** - determines the type of the regions that are extracted. If 'dark' - only MSERs that are darker than their surroundings are extracted. If 'light' - only lighter.

*Default:* 'both' (both types of MSERs are extracted)

*List of values:* 'light', 'dark', 'both'

**minArea** - minimal size of an MSER.

*Default:* 10

*Suggested of values:* 1, 10, 100, 10000

**maxArea** - maximal size of an MSER.

*Default:* 10000

*Suggested values:* 1, 10, 100, 10000

**channel** - as segment_mser is used to single-channel image only, it's necessary to choose one channel, if segmenting image is multichannel

*Default:* 1

**delta** - amount of thresholds for which a region needs to be stable. It influences the selectivity of the algorithm. Larger values lead to fewer MSERs. Smaller values lead to more MSERs.

*Default:* 15

*Suggested values:* 5, 10, 20, 50

**max_variation** - the maximum variation of a component's area within the range of *delta* thresholds. Larger values lead to more MSERs. Smaller values lead to fewer MSERs.

*Default:* 0.2

*Suggested values:* 0.1, 0.2, 0.5, 1.0, 2.0, 5.0 (*max_variation* >= 0)

**min_diversity** - The minimum relative difference of the sizes of two overlapping MSERs. Smaller values lead to more overlapping MSERs. Larger values lead to fewer overlapping MSERs.

*Default:* 0.8

*Suggested values:* 0.1, 0.5, 0.8, 1.0, 2.0, 5.0 (*min_diversity* >= 0)

**may_touch_border** - Controls if regions that touch the border of the input domain are returned ('true') or rejected ('false').

*Default:* 'false'

*List of values:* 'false', 'true'

 
Output
--------
**MSERDark** - region marked with red

**MSERLight** - region marked with green

Each of them may be used in further imager processing ex. shape measurement.
