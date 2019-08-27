# <p align="right"><a class="github-button" aria-label="Download ntkme/github-buttons on GitHub" href="https://github.com/Balluff-BVS/halconscripts/raw/master/Filters/Inpainting/inpainting_filters.zip" data-icon="octicon-cloud-download">Download</a></p>


INPAINTING MCF
==========

## Example

Original Picture             | Filtered Picture
:-------------------------:|:-------------------------:
![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Filters/Inpainting/InpaintingMcf/original.png?raw=true)  |  ![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Filters/Inpainting/InpaintingMcf/inpainting_mcf.png?raw=true)

Description
----------

Perform an inpainting by smoothing of level lines.

The operator inpainting_mcf extends the image edges that adjoin the region of the input image into the interior of region and connects their ends by smoothing the level lines of the gray value function of image.

Input Parameters
----------

**Sigma** - Smoothing for derivative operator.

*Default value:* 0.5

*Suggested values:*  0.0, 0.1, 0.5, 1.0

*Restriction:* Sigma >= 0

**Theta** - Time step.

*Default value:* 0.5

*Suggested values:*  0.1, 0.2, 0.3, 0.4, 0.5

*Restriction:* 0 < Theta <= 0.5

**Iterations** - Number of iterations.

*Default value:* 10

*Suggested values:*  1, 5, 10, 20, 50, 100, 500

*Restriction:* Iterations >= 1
