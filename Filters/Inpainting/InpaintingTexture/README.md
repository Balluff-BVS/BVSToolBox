# <p align="right"><a class="github-button" aria-label="Download ntkme/github-buttons on GitHub" href="https://github.com/Balluff-BVS/halconscripts/raw/master/Filters/Inpainting/inpainting_filters.zip" data-icon="octicon-cloud-download">Download</a></p>


INPAINTING TEXTURE
==========

## Example

Original Picture             | Filtered Picture
:-------------------------:|:-------------------------:
![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Filters/Inpainting/InpaintingTexture/original.png?raw=true)  |  ![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Filters/Inpainting/InpaintingTexture/inpainting_texture.png?raw=true)

Description
----------

Perform an inpainting by texture propagation.

The operator inpainting_texture is used for removing large objects and image errors from the region of the input image. Image blocks of side length *MaskSize* are copied from the intact part of the image to the border of the computation area, until that area has been filled up with new gray values.

Input Parameters
----------

**MaskSize** - Size of the inpainting blocks.

*Default value:* 9

*Suggested values:*  7, 9, 11, 15, 21

*Restriction:* MaskSize >= 3 (MaskSize is odd value)

**SearchSize** - Size of the search window.

*Default value:* 30

*Suggested values:*  15, 30, 50, 100, 1000

*Restriction:* 2 x SearchSize > MaskSize

**Anizotropy** - Influence of the edge amplitude on the inpainting order.

*Default value:* 1.0

*Suggested values:*  0.0, 0.01, 0.1, 0.5, 1.0, 10.0

*Restriction:* Anisotropy >= 0

**PostIteration** - Post-iteration for artifact reduction.

*Default value:* 'none'

*List of values:*  'min_grad', 'min_range_extension', 'none'

**Smoothness** - Gray value tolerance for post-iteration.

*Default value:* 1.0

*Suggested values:*  0.0, 0.1, 0.2, 0.5, 1.0

*Restriction:* Smoothness >= 0

