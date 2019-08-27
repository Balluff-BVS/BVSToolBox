# <p align="right"><a class="github-button" aria-label="Download ntkme/github-buttons on GitHub" href="https://github.com/Balluff-BVS/halconscripts/raw/master/Filters/Inpainting/inpainting_filters.zip" data-icon="octicon-cloud-download">Download</a></p>


INPAINTING CT
==========

## Example

Original Picture             | Filtered Picture
:-------------------------:|:-------------------------:
![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Filters/Inpainting/InpaintingCt/original.png?raw=true)  |  ![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Filters/Inpainting/InpaintingCt/inpainting_ct.png?raw=true)

Description
----------

Perform an inpainting by coherence transport.

The operator inpainting_ct inpaints a missing region of an image by transporting image information from the region's boundary along the coherence direction into this region.

Input Parameters
----------

**Epsilon** - Radius of the pixel neighborhood.

*Default value:* 5.0

*Range of values:*  1.0 <= Epsilon <= 20.0

**Kappa** - Sharpness parameter in percent.

*Default value:* 25.0

*Range of values:*  0 <= Kappa <= 100.0

**Sigma** - Pre-smoothing parameter.

*Default value:* 1.41

*Range of values:*  0 <= Sigma <= 20.0

**Rho** - Smoothing parameter for the direction estimation.

*Default value:* 4.0

*Range of values:*  0.001 <= Rho <= 20.0

**ChannelCoefficients** - Channel weights.

*Default value:* 1
