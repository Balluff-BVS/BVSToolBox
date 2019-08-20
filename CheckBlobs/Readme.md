# <p align="right"><a class="github-button" aria-label="Download ntkme/github-buttons on GitHub" href="https://github.com/Balluff-BVS/TestScripts/raw/master/CheckBlobs/check_blobs.zip" data-icon="octicon-cloud-download">Download</a></p>

CHECK BLOBS
===========
Example
---------
<p align="center">
  <img src="https://github.com/Balluff-BVS/TestScripts/blob/master/CheckBlobs/check_blobs.png?raw=true" alt="Picture error">
</p>

Description
----------
Extracts regions from image using given threshold and region features, ex.: area, circularity, height etc. 

Enables pointing one region and displaying 10 of its feature values.

Input parameters
----------
 * Features - shape features to be checked
 * Operation - linkage type of the individual features
 * Min_Values / Max_Values - limits of the features
 * MinGray / MaxGray - threshold for the gray values
 * region_to_measure - index of region which parameters are displayed
 * sort_mode - kind of sorting
 * row_or_col - sorting first with respect to row, then to column, or otherwise
 * Parametr [0-9] - choose shape features to be measured and displayed as output

**SHAPE FEATURES:**

 * area
 * row - Row index of the center
 * column - Column index of the center
 * width - Width of the region (parallel to the coordinate axes)
 * height - Height of the region (parallel to the coordinate axes)
 * ratio - Ratio of the height and the width of the region (parallel to the coordinate axes)
 * circularity
 * compactness
 * contlength - Total length of contour
 * convexity
 * rectangularity
 * ra - Main radius of the equivalent ellipse
 * rb - Secondary radius of the equivalent ellipse
 * phi - Orientation of the equivalent ellipse
 * anisometry
 * bulkiness
 * struct_factor
 * outer_radius - Radius of smallest surrounding circle
 * inner_radius - Radius of largest inner circle
 * inner_width - Width of the largest axis-parallel rectangle that fits into the region
 * inner_height - Height of the largest axis-parallel rectangle that fits into the region
 * dist_mean - Mean distance from the region border to the center
 * dist_deviation - Deviation of the distance from the region border to the center
 * roundness
 * num_sides - Number of polygon sides
 * connect_num
 * max_diameter - Maximum diameter of the region
 * orientation - Orientation of the region
 * euler_number
 * rect2_phi - Orientation of the smallest surrounding rectangle
 * rect2_len2 - Half the length of the smallest surrounding rectangle
 * rect2_len2 - Half the width of the smallest surrounding rectangle
 * moments_m11 - Product of inertia of the axes through the center parallel to the coordinate axes.
 * moments_m20 - Moment of 2nd order (row-dependent).
 * moments_m02 - Moment of 2nd order (column-dependent).
 * moments_ia - Length of the major axis of the input region.
 * moments_ib - Length of the minor axis of the input region.

Output
---------
Collection of regions selected from image.

10 chosen parameters of a single region marked with red pointer.


