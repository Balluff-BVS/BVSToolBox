# <p align="right"><a class="github-button" aria-label="Download ntkme/github-buttons on GitHub" href="https://github.com/Balluff-BVS/halconscripts/raw/master/Filters/Enhacement/enhancement_filters.zip" data-icon="octicon-cloud-download">Download</a></p>

COHERENCE ENHANCING DIFF
==========

## Example

Original Picture             | Filtered Picture
:-------------------------:|:-------------------------:
![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Filters/Enhacement/CoherenceEnhancingDiff/original.png?raw=true)  |  ![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Filters/Enhacement/CoherenceEnhancingDiff/coherence_enhancing_diff.png?raw=true)

Description
----------

Performs an anisotropic diffusion process on the input image to increase the coherence of the image structures.

To detect the edge direction more robustly, in particular on noisy input data, an additional isotropic smoothing step can precede the computation of the gray value gradients. The parameter *Sigma* determines the magnitude of the smoothing by means of the standard deviation of a corresponding Gaussian convolution kernel.

Input Parameters
----------

**Sigma** - Smoothing for derivative operator.

*Default value:* 0.5

*Suggested values:* 0.0, 0.1, 0.5, 1.0

*Restriction:* 0 <= Sigma

**Rho** - Smoothing for diffusion coefficients.

 *Default value:* 3.0
 
*Suggested values:* 0.0, 1.0, 3.0, 5.0, 10.0, 30.0

*Restriction:* Rho >= 0

**Tho** - Time step.

 *Default value:* 0.5
 
*Suggested values:* 0.1, 0.2, 0.3, 0.4, 0.5

**Restriction:* 0 <= Theta <= 0.5

**Interations** - Number of iterations.

 *Default value:* 10
 
*Suggested values:* 1, 5, 10, 20, 50, 100, 500

*Restriction:* Interations >= 1


.
