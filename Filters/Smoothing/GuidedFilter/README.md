# <p align="right"><a class="github-button" aria-label="Download ntkme/github-buttons on GitHub" href="https://github.com/Balluff-BVS/halconscripts/raw/master/Filters/Smoothing/GuidedFilter/guided_filter.zip" data-icon="octicon-cloud-download">Download</a></p>


GUIDED FILTER
==========

## Example

Original Picture             | Filtered Picture
:-------------------------:|:-------------------------:
![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Filters/Smoothing/GuidedFilter/original.png?raw=true)  |  ![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Filters/Smoothing/GuidedFilter/guided_filter.png?raw=true)

Description
----------

Filters the input image using the guidance image guide. 

If image and image guide are identical, guided_filter behaves like an edge-preserving smoothing with a filter mask with Radius. Pixels at edges that have a contrast significantly greater than Amplitude are preserved, while pixels in homogeneous areas are smoothed. Hence, guided_filter is a fast alternative to anisotropic_diffusion or bilateral_filter.

If image and image guide are different, image is smoothed with a filter mask with Radius, except in areas where image guide has edges with a contrast significantly greater than Amplitude.

Input Parameters
----------

**Radius** - Radius of the filtering operation.

*Default value:* 3

*Suggested values:* 1, 2, 3, 5, 10

*Restriction:* 0 < Radius

**Amplitude** - Controls the influence of edges on the smoothing.

*Default value:* 20

*Suggested values:* 3.0, 10.0, 20.0, 50.0, 100.0

*Restriction:* 0 < Amplitude
