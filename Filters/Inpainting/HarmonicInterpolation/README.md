# <p align="right"><a class="github-button" aria-label="Download ntkme/github-buttons on GitHub" href="https://github.com/Balluff-BVS/TestScripts/raw/master/Filters/Inpainting/inpainting_filters.zip" data-icon="octicon-cloud-download">Download</a></p>


HARMONIC INTERPOLATION
==========

## Example

Original Picture             | Filtered Picture
:-------------------------:|:-------------------------:
![Image error](https://github.com/Balluff-BVS/TestScripts/blob/master/Filters/Inpainting/HarmonicInterpolation/original.png?raw=true)  |  ![Image error](https://github.com/Balluff-BVS/TestScripts/blob/master/Filters/Inpainting/HarmonicInterpolation/harmonic_interpolation.png?raw=true)

Description
----------

Perform a harmonic interpolation on an image region.

The operator harmonic_interpolation reconstructs the destroyed image data of inside the region by solving the discrete Laplace equation for the corresponding gray value function. The unique solution, which exists under Dirichlet boundary conditions given by image outside of region, is returned in InpaintedImage. This technique is called harmonic interpolation since in function theory the solutions of the Laplace equation are referred to as harmonic functions.

Input Parameters
----------

**Precision** - Computational accuracy.

*Default value:* 0.001

*Suggested values:* 0.0, 0.0001, 0.001, 0.01

*Restriction:* 0 <= Precision (both values are odd)
