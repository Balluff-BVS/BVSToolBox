# <p align="right"><a class="github-button" aria-label="Download ntkme/github-buttons on GitHub" href="https://github.com/Balluff-BVS/TestScripts/raw/master/Filters/Inpainting/inpainting_filters.zip" data-icon="octicon-cloud-download">Download</a></p>


INPAINTING ANISO
==========

## Example

Original Picture             | Filtered Picture
:-------------------------:|:-------------------------:
![Image error](https://github.com/Balluff-BVS/TestScripts/blob/master/Filters/Inpainting/InpaintingAniso/original.png?raw=true)  |  ![Image error](https://github.com/Balluff-BVS/TestScripts/blob/master/Filters/Inpainting/InpaintingAniso/inpainting_aniso.png?raw=true)

Description
----------

Perform an inpainting by anisotropic diffusion.

The operator inpainting_aniso uses the anisotropic diffusion according to the model of Perona and Malik, to continue image edges that cross the border of the region and to connect them inside of region.

Input Parameters
----------

**Mode** - Type of edge sharpening algorithm.

*Default value:* 'weickert'

*Suggested values:*  'parabolic', 'perona-malik', 'shock', 'weickert'

**Contrast** - Contrast parameter.

*Default value:* 5.0

*Suggested values:*  0.5, 2.0, 5.0, 10.0, 20.0, 50.0, 100.0

*Restriction:* Contrast > 0

**Theta** - Step size.

*Default value:* 5.0

*Suggested values:*  0.5, 2.0, 5.0, 10.0, 20.0, 50.0, 100.0

*Restriction:* Theta > 0

**Iterations** - Number of iterations.

*Default value:* 10

*Suggested values:*  1, 3, 10, 100, 500

*Restriction:* Iterations >= 1

**Rho** - Smoothing coefficient for edge information.

*Default value:* 3.0

*Suggested values:*  0.0, 0.1, 0.5, 1.0, 3.0, 10.0

*Restriction:* Rho >= 1
