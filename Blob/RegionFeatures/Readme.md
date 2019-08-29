# <p align="right"><a class="github-button" aria-label="Download ntkme/github-buttons on GitHub" href="https://github.com/Balluff-BVS/halconscripts/raw/master/Blob/RegionFeatures/region_features.zip" data-icon="octicon-cloud-download">Download</a></p>

REGION FEATURES
===========
Example
---------
<p align="center">
  <img src="https://github.com/Balluff-BVS/halconscripts/blob/master/Blob/RegionFeatures/region_info.PNG?raw=true" alt="Picture error">
</p>

Description
----------

Select regions according to indicated features.

**regionInfo_one_region** - returns 10 indicated parameters of one of selected regions, marked with red pointer

**regionInfo_multiple_regions** - returns the value of one chosen parameter of all selected regions

Input parameters
----------
**FeaturesSelection** - features to be checked when selecting regions

*Default:* 'area'

**Operation** - linkage type of the individual features

*Default:* 'and'

*List of values:* 'and', 'or'

**Min_Values / Max_Values** - limits of the features

*Default:* Min_Value = 150, Max_Value = 99999

*Range of values:* (0,99999)

**sort_mode** - kind of sorting

*Default:* 'first_point'

*List of values:* 'character', 'first_point', 'last_point', 'lower_left', 'lower_right', 'upper_left', 'upper_right'

**row_or_col** - sorting first with respect to row, then to column, or otherwise

*Default:* 'row'

*List of values:* 'column', 'row'

**Parameters for *regionInfo_one_region* only:**

**region_to_measure** - index of region which parameters are displayed

*Default:* 0

**Parametr [0-9]** - choose shape features to be measured and displayed as output

**Parameters for *regionInfo_multiple_region* only:**

**Feature_toPrint** - region feature which value is put into output array

*Default:* 'area'

**ArrayCount** - number of elements in the output array

*Default:* 10

*Range of values:* (0, 32)

**POSSIBLE FEATURES:**

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

*regions_number* - number of selected regions

**regionInfo_one_region** - 10 chosen parameters of a single region marked with red pointer (named *Parameter0_Val*, *Parametr1_Val* etc.); current coordinates of the pointer (*pointer_X, pointer_Y*)

**regionInfo_multiple_regions** - an array *Parameters* of values of an indicated parameter (*Feature_toPrint*)


