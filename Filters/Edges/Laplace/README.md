# <p align="right"><a class="github-button" aria-label="Download ntkme/github-buttons on GitHub" href="https://github.com/Balluff-BVS/halconscripts/raw/master/Filters/Edges/edges_filters.zip" data-icon="octicon-cloud-download">Download</a></p>


LAPLACE OPERATOR
==========

## Example

Original             | Edges Direction
:-------------------------:|:-------------------------:
![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Filters/Edges/Laplace/original.png?raw=true)  |  ![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Filters/Edges/Laplace/laplace_filter.png?raw=true)

Description
----------

Calculate the Laplace operator by using finite differences.

Input parameters
---------------

**MaskSize** - Size of filter mask.

*Default value:* 3

*List of values:* 3, 5, 7, 9, 11, 13, 15, 17, 19, 21, 23, 25, 27, 29, 31, 33, 35, 37, 39

**FilterMask** - Filter mask used in the Laplace operator.

*Default:* 'n_4'

*List of values:* 'n_4', 'n_8', 'n_8_isotropic'
