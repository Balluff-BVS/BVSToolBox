# <p align="right"><a class="github-button" aria-label="Download ntkme/github-buttons on GitHub" href="https://github.com/Balluff-BVS/halconscripts/raw/master/Blob/LocalThreshold/local_threshold.zip" data-icon="octicon-cloud-download">Download</a></p>

LOCAL THRESHOLD
===========
Example
---------
Original Picture             | Thresholded Picture
:-------------------------:|:-------------------------:
![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Blob/LocalThreshold/original.png?raw=true)  |  ![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Blob/LocalThreshold/local_threshold.png?raw=true)

Description
----------
Segments a single-channel image using the thresholding method 'adapted_std_deviation' and returns the segmented region. 
The algorithm is able to segment document images even if they are degraded, e.g., due to inhomogeneous illumination or noise. It enables text binarization on an inhomogeneous background by taking into account the local contrast.

Input parameters
----------
 **light_dark** - controls whether light or dark structures are segmented. If 'dark', dark structures on a light background are segmented. If 'light' - the other way round (The result is essentially the same as if the image would have been inverted and then the parameter was set to 'dark'.)
 
 *Default:* 'dark'
 
 *Suggested values:* 'dark', 'light'
 
 **mask_size** - specifies the mask size, i.e., the size of the neighborhood in which the local threshold is calculated. The smaller the window size the thinner the segmented strokes. 'mask_size' must be set to a value that is larger than the stroke width of the characters or structures to be segmented. If 'mask_size' is even, the next larger odd value is used.
 
 *Default:* 15
 
 *Suggested values:* 15, 21, 31
 
 **scale** - controls how much the threshold value differs from the local mean value. Use smaller values for 'scale' to also segment structures with a lower contrast to their background. Use larger values to suppress clutter.
 
 *Default:* 0.2
 
 *Suggested values:* 0.2, 0.3, 0.5
 
Output
--------
Segmented output region, that can be used in further image processing ex. finding object or measuring shape.
