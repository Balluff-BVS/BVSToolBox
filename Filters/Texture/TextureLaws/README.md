# <p align="right"><a class="github-button" aria-label="Download ntkme/github-buttons on GitHub" href="https://github.com/Balluff-BVS/halconscripts/raw/master/Filters/Texture/texture_filters.zip" data-icon="octicon-cloud-download">Download</a></p>


TEXTURE LAWS
==========

## Example

Original Picture             | Filtered Picture
:-------------------------:|:-------------------------:
![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Filters/Texture/TextureLaws/original.png?raw=true)  |  ![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/Filters/Texture/TextureLaws/texture_laws.png?raw=true)

Description
----------

Filter an image using a Laws texture filter.

Function applies a texture transformation to an image. This is done by convolving the input image with a special filter mask.

Input Parameters
----------

**FilterTypes** - Desired filter. The names of the filters are mnemonics for “level,” “edge,” “spot,” “wave,” “ripple,” “undulation,” and “oscillation.” The name of the filter is composed of the letters of the two vectors used, where the first letter denotes convolution in the column direction while the second letter denotes convolution in the row direction.

*Default value:* 'el'

*Suggested values:* 'll', 'le', 'ls', 'lw', 'lr', 'lu', 'lo', 'el', 'ee', 'es', 'ew', 'er', 'eu', 'eo', 'sl', 'se', 'ss', 'sw', 'sr', 'su', 'so', 'wl', 'we', 'ws', 'ww', 'wr', 'wu', 'wo', 'rl', 're', 'rs', 'rw', 'rr', 'ru', 'ro', 'ul', 'ue', 'us', 'uw', 'ur', 'uu', 'uo', 'ol', 'oe', 'os', 'ow', 'or', 'ou', 'oo'

**Shift** - Shift to reduce the gray value dynamics. For most of the filters the resulting gray values must be modified by a Shift. This makes the different textures in the output image more comparable to each other, provided suitable filters are used.

*Default value:* 2

*Suggested values:* 0, 1, 2, 3, 4, 5, 6, 7, 8, 9

**FilterSize** - Size of the filter kernel.

*Default value:* 5

*Suggested values:* 3, 5, 7
