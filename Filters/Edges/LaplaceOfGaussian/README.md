# <p align="right"><a class="github-button" aria-label="Download ntkme/github-buttons on GitHub" href="https://github.com/Balluff-BVS/halconscripts/raw/master/Filters/Edges/edges_filters.zip" data-icon="octicon-cloud-download">Download</a></p>


LAPLACE OF GAUSSIAN
==========

## Example

Original Picture             | Edges
:-------------------------:|:-------------------------:
![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Filters/Edges/LaplaceOfGaussian/original.png?raw=true)  |  ![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Filters/Edges/LaplaceOfGaussian/laplace_of_gauss.png?raw=true)

Description
----------

**laplace_of_gauss** calculates the Laplace-of-Gaussian operator, i.e., the Laplace operator on a Gaussian smoothed image, for arbitrary smoothing parameters *Sigma*. 

**diff_of_gauss** approximates the Laplace-of-Gauss operator by a difference of Gaussians. The standard deviations of these Gaussians can be calculated, according to Marr, from the parameter *Sigma* of the LoG and the ratio of the two standard deviations.

Input Parameters
----------

**Sigma** - Smoothing parameter.

*Default value:* 3 (for *diff_of_gauss*), 2 (for *laplace_of_gauss*)

*Suggested values:* 2.0, 3.0, 4.0, 5.0 (for *diff_of_gauss*)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
0.5, 1.0, 1.5, 2.0, 2.5, 3.0, 4.0, 5.0, 7.0 (for *laplace_of_gauss*)

**SigFactor** - Ratio of the standard deviations used. (for *diff_of_gauss* function)

*Default value:* 1.6

*Range of values:* 0.1 <= SigFactor <= 10.0

*Restriction:* 0 < SigFactor
