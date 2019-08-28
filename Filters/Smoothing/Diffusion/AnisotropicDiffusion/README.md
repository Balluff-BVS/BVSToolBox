# <p align="right"><a class="github-button" aria-label="Download ntkme/github-buttons on GitHub" href="https://github.com/Balluff-BVS/TestScripts/raw/master/Filters/Smoothing/Diffusion/AnisotropicDiffusion/anisotropic_diffusion.zip" data-icon="octicon-cloud-download">Download</a></p>


ANISOTROPIC DIFFUSION
==========

## Example

Original Picture             | Filtered Picture
:-------------------------:|:-------------------------:
![Image error](https://github.com/Balluff-BVS/TestScripts/blob/master/Filters/Smoothing/Diffusion/AnisotropicDiffusion/original.png?raw=true)  |  ![Image error](https://github.com/Balluff-BVS/TestScripts/blob/master/Filters/Smoothing/Diffusion/AnisotropicDiffusion/anisotropic_diffusion.png?raw=true)

Description
----------

The operator anisotropic_diffusion performs an anisotropic diffusion on the input image Image according to the model of Perona and Malik. 

The goal of the anisotropic diffusion is the elimination of image noise in constant image patches while preserving the edges in the image.

Input Parameters
----------

**Mode** - Diffusion coefficient as a function of the edge amplitude.

*Default value:* 'weickert'

*List of values:*  'parabolic', 'perona-malik', 'weickert'

**Contrast** - Contrast parameter.

*Default value:* 5

*Suggested values:* 2.0, 5.0, 10.0, 20.0, 50.0, 100.0

*Restriction:* Contrast > 0

**Theta** - Time step.

*Default value:* 1

*Suggested values:* 0.5, 1.0, 3.0

**Iterations** - Number of iterations.

*Default value:* 10

*List of values:* 1.0, 2.0, 5.0, 10.0

*Restriction:* Iterations > 1
