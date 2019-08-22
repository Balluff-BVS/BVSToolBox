# <p align="right"><a class="github-button" aria-label="Download ntkme/github-buttons on GitHub" href="https://github.com/Balluff-BVS/TestScripts/raw/master/EdgesImage/edges_image.zip" data-icon="octicon-cloud-download">Download</a></p>

EDGES IMAGE 
=============

## Example

Original Picture             | Extracted Edges
:-------------------------:|:-------------------------:
![Image error](https://github.com/Balluff-BVS/TestScripts/blob/master/EdgesImage/original.png?raw=true)  |  ![Image error](https://github.com/Balluff-BVS/TestScripts/blob/master/EdgesImage/edges_image.png?raw=true)

Description
------------

Detects step edges using recursively implemented filters (according to Deriche, Lanser and Shen) or the conventionally implemented “derivative of Gaussian” filter (using filter masks) proposed by Canny. Furthermore, a very fast variant of the Sobel filter can be used.

Input parameters
-----------------

**filter** - edge operator to be applied.

*Default:* 'canny'

*List of values:* 'canny', 'deriche1', 'deriche1_int4', 'deriche2', 'deriche2_int4', 'lanser1', 'lanser2', 'mshen', 'shen', 'sobel_fast'

**alpha** - filter parameter: small values result in strong smoothing, and thus less detail

*Default:* 1.0

*Suggested values:* 0.1, 0.2, 0.3, 0.4, 0.5, 0.7, 0.9, 1.1 (0.2 <= alpha <= 50.0)

**NMS** - non-maximum suppression ('none', if not desired)

*Default:* 'nms'

*Suggested values:* 'hvnms', 'inms', 'nms', 'none'

**low** - lower threshold for the hysteresis threshold operation (negative, if no thresholding is desired).

*Default:* 20

*Suggested values:* 5, 10, 15, 20, 25, 30, 40 (1 <= low <= 255)

**high** - upper threshold for the hysteresis threshold operation (negative, if no thresholding is desired).

*Default:* 40

*Suggested values:* 10, 15, 20, 25, 30, 40, 50, 60, 70 (1 <= high <= 255)

Output
-------------

Contour with extracted edges.

