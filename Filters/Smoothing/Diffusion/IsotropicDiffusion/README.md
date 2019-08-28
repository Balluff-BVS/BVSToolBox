# <p align="right"><a class="github-button" aria-label="Download ntkme/github-buttons on GitHub" href="https://github.com/Balluff-BVS/halconscripts/raw/master/Filters/Smoothing/Diffusion/IsotropicDiffusion/isotropic_diffusion.zip" data-icon="octicon-cloud-download">Download</a></p>


ISOTROPIC DIFFUSION
==========

## Example

Original Picture             | Filtered Picture
:-------------------------:|:-------------------------:
![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Filters/Smoothing/Diffusion/IsotropicDiffusion/original.png?raw=true)  |  ![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Filters/Smoothing/Diffusion/IsotropicDiffusion/isotropic_diffusion.png?raw=true)

Description
----------

The operator isotropic_diffusion performs an isotropic diffusion of the input image. This corresponds to a convolution of the image matrix with a Gaussian mask of standard deviation *Sigma*. If the parameter *Iterations* is set to 0, such a convolution is performed explicitly.

Input Parameters
----------

**Sigma** - Standard deviation of the Gauss distribution.

*Default value:* 1

*Suggested values:* 0.1, 0.5, 1.0, 3.0, 10.0, 20.0, 50.0

*Restriction:* Sigma > 0

**Iterations** - Number of iterations.

*Default value:* 10

*Suggested values:* 0, 3, 10, 100, 500

*Restriction:* Iterations >= 0
