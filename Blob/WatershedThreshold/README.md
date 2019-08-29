# <p align="right"><a class="github-button" aria-label="Download ntkme/github-buttons on GitHub" href="https://github.com/Balluff-BVS/halconscripts/raw/master/Blob/WatershedThreshold/watershed_threshold.zip" data-icon="octicon-cloud-download">Download</a></p>

LOCAL THRESHOLD
===========
Example
---------

<p align="center">
  <img src="https://github.com/Balluff-BVS/halconscripts/blob/master/Blob/WatershedThreshold/watershed_threshold.png?raw=true" alt="Picture error">
</p>

Description
----------

Watersheds segments an image based on the topology of the gray values. The image is interpreted as a “mountain range.” Higher gray values correspond to “mountains,” while lower gray values correspond to “valleys.” In the resulting mountain range watersheds are extracted. These correspond to the bright ridges between dark basins. On output, the parameter Basins contains these basins, while Watersheds contains the watersheds, which are at most one pixel wide. Watersheds always is a single region per input image, while Basins contains a separate region for each basin.

In the function watershed_threshold, the basins are successively merged if they are separated by a watershed that is smaller than *Threshold*.

Input parameters
----------
**For *watershed_threshold* only:**

**Threshold** - Threshold for the watersheds.

*Default:* 50

*Range of values:* (1,255)
 
Output
--------

*Basins* (region) - segmented basins

*Watersheds* (region) - watersheds between the basins
