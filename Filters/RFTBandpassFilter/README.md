# <p align="right"><a class="github-button" aria-label="Download ntkme/github-buttons on GitHub" href="https://github.com/Balluff-BVS/halconscripts/raw/master/Filters/RFTBandpassFilter/rft_bandpass_filter.zip" data-icon="octicon-cloud-download">Download</a></p>


RFT BANDPASS FILTER
==========

## Example

Original Picture             | Filtered Picture
:-------------------------:|:-------------------------:
![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Filters/RFTBandpassFilter/original.png?raw=true)  |  ![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Filters/RFTBandpassFilter/rft_bandpass_filter.png?raw=true)

Description
----------

Generate a bandpass filter with sinusoidal shape using real-values fast Fourier transform.

Enables selecting regions from filtered image.

Input Parameters
----------

**filter_freq** - The maximum of the sinusoidal function

*Default value:* 0.1

*Suggested values:*  0.0, 0.1, 0.2, 0.3, 0.4, 0.5, 0.6, 0.7, 0.8, 0.9, 1.0

*Restriction:* filter_freq >= 0

**shape_area_min** - Lower limits of the features.

*Default value:* 150

*Range of values:* 0 <= shape_area_min <= 99999

**shape_area_max** - Upper limits of the features.

*Default value:* 99999

*Range of values:* 0 <= shape_area_min <= shape_area_max <= 99999

**features** - Shape features to be checked.

*Default value:* 'area'

*List of values:* 'anisometry', 'area', 'area_holes', 'bulkiness', 'circularity', 'column', 'column1', 'column2', 'compactness', 'connect_num', 'contlength', 'convexity', 'dist_deviation', 'dist_mean', 'euler_number', 'height', 'holes_num', 'inner_height', 'inner_radius', 'inner_width', 'max_diameter', 'moments_i1', 'moments_i2', 'moments_i3', 'moments_i4', 'moments_ia', 'moments_ib', 'moments_m02', 'moments_m02_invar', 'moments_m03', 'moments_m03_invar', 'moments_m11', 'moments_m11_invar', 'moments_m12', 'moments_m12_invar', 'moments_m20', 'moments_m20_invar', 'moments_m21', 'moments_m21_invar', 'moments_m30', 'moments_m30_invar', 'moments_phi1', 'moments_phi2', 'moments_psi1', 'moments_psi2', 'moments_psi3', 'moments_psi4', 'num_sides', 'orientation', 'outer_radius', 'phi', 'ra', 'ratio', 'rb', 'rect2_len1', 'rect2_len2', 'rect2_phi', 'rectangularity', 'roundness', 'row', 'row1', 'row2', 'struct_factor', 'width'

**operation** - Linkage type of the individual features.

*Default value:* 'and'

*List of values:* 'and', 'or'
