# <p align="right"><a class="github-button" aria-label="Download ntkme/github-buttons on GitHub" href="https://github.com/Balluff-BVS/halconscripts/raw/master/Filters/Inpainting/inpainting_filters.zip" data-icon="octicon-cloud-download">Download</a></p>


INPAINTING CED
==========

## Example

Original Picture             | Filtered Picture
:-------------------------:|:-------------------------:
![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Filters/Inpainting/InpaintingCed/original.png?raw=true)  |  ![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Filters/Inpainting/InpaintingCed/inpainting_ced.png?raw=true)

Description
----------

Perform an inpainting by coherence enhancing diffusion.

The operator inpainting_ced performs an anisotropic diffusion process on the region of the input image with the objective of completing discontinuous image edges diffusively by increasing the coherence of the image structures contained in image and without smoothing these edges perpendicular to their dominating direction.

Input Parameters
----------

**Sigma** - Smoothing for derivative operator.

*Default value:* 0.5

*Suggested values:*  0.0, 0.1, 0.5, 1.0

*Restriction:* Sigma >= 0

**Rho** - Smoothing for diffusion coefficients.

*Default value:* 3.0

*Suggested values:*  0.0, 1.0, 3.0, 5.0, 10.0, 30.0

*Restriction:* Rho >= 0

**Theta** - Time step.

*Default value:* 0.5

*Suggested values:*  0.1, 0.2, 0.3, 0.4, 0.5

*Restriction:* 0 < Theta <= 0.5

**Iterations** - Number of iterations.

*Default value:* 10

*Suggested values:*  1, 5, 10, 20, 50, 100, 500

*Restriction:* Iterations >= 1
