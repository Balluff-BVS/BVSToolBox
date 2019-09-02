# <p align="right"><a class="github-button" aria-label="Download ntkme/github-buttons on GitHub" href="https://github.com/Balluff-BVS/halconscripts/raw/master/ShapeMatching/shape_matching.zip" data-icon="octicon-cloud-download">Download</a></p>

SHAPE MATCHING
==============

## Example

Teaching Picture             | Shape Matching
:-------------------------:|:-------------------------:
![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/ShapeMatching/teach_image.PNG?raw=true)  |  ![Image error](https://github.com/Balluff-BVS/halconscripts/blob/master/ShapeMatching/search_image.PNG?raw=true)

Description
-----------

**save_shape_matching_model** - Performs model teaching from given input (mask and reference image, input region or .dxf file) 
Created shape model can be saved in default directory on industrial controller or in User's directory, when working with BVS Cockpit installed on PC.

**use_shape_matching_model** - Read previously saved shape model from specific directory and uses it to find matching shapes on image.
Image is searched in given region of interest - *inputAOI*.
Get parameters such as: center coordinates, rotation angle, scale and matching score of found shapes. 

Input parameters
----------------

<p align="center"><b>
  Parameters for both <i>use_shape_matching_model</i> and <i>save_shape_matching_model</i>:
</b></p>

**AngleStart, AngleStop** - Extent of the rotation angles.

*Default value:* 0 (for AngleStart), 6.29 (for AngleStop)

*Suggested values:* -3.14, -1.57, -0.79, -0.39, -0.20, 0.0 (for AngleStart)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
6.29, 3.14, 1.57, 0.79, 0.39, 0.0 (for AngleStop)

**ScaleMin, ScaleMax** - scale of the models.

*Default value:* 0.1 (for ScaleMin), 1.0 (for ScaleMax)

*Suggested values:* 0.5, 0.6, 0.7, 0.8, 0.9, 1.0 (for ScaleMin)
  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
1.0, 1.1, 1.2, 1.3, 1.4, 1.5 (for ScaleMax)

*Restriction:* ScaleMin > 0, ScaleMax >= ScaleMin

**ModelImage_Scale** - scale used in save_shape_matching_model_dxf to transform read contours into output image.

**filename** - name of file to save/read. Format .shm is added automatically while saving/reading. In save_shape_matching_model_dxf there are two filenames: *filename_contours* for .dxf file to read and *filename_model* for shape model to save.

**file_directory** - path to the file to save/read. As default it is set as */data/icsServer/share/images/*, 
which leads to folder in industrial controller memory. User can customize the path by filling in *file_directory* field, when working 
with BVS Cockpit installed on PC. In save_shape_matching_model_dxf there are two filepaths: *file_directory_contours* for .dxf file to read and *file_directory_model* for shape model to save.

<p align="center"><b>
  Parameters for <i>use_shape_matching_model</i> only:
</b></p>

**inputAOI** - Rectangular region of interest.

*startX, startY* - coordinates of upper left corner of region

*width, heght* - dimensions of rectangular region.

**ArrayCount** - number of found shapes to return in output array

*Default value:* 3

*Range of values:* 1 <= ArrayCount <= 32

**ObjectPointer** - index of shape to be pointed in the picture with purple cross

**MinScore** - Minimum score of the instances of the models to be found.

*Default value:* 0.5

*Suggested values:* 0.3, 0.4, 0.5, 0.6, 0.7, 0.8, 0.9, 1.0

*Typical range of values:* 0 <= MinScore <= 1

**NumMatches** - Number of instances of the models to be found (or 0 for all matches).

*Default value:* 0

*Suggested values:* 0, 1, 2, 3, 4, 5, 10, 20

**MaxOverlap** - Maximum overlap of the instances of the models to be found.

*Default value:* 0.5

*Suggested values:* 0.0, 0.1, 0.2, 0.3, 0.4, 0.5, 0.6, 0.7, 0.8, 0.9, 1.0

*Typical range of values:* 0 <= MaxOverlap <= 1

**SubPixel** - Subpixel accuracy if not equal to 'none'.

*Default value:* 'least_squares'

*Suggested values:* 'none', 'interpolation', 'least_squares', 'least_squares_high', 'least_squares_very_high', 'max_deformation 1', 'max_deformation 2', 'max_deformation 3', 'max_deformation 4', 'max_deformation 5', 'max_deformation 6'

**NumLevels** - Number of pyramid levels used in the matching (and lowest pyramid level to use if |NumLevels| = 2).

*Default value:* 0

*List of values:* 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10

**Greediness** - “Greediness” of the search heuristic (0: safe but slow; 1: fast but matches may be missed).

*Default value:* 0.9

*Suggested values:* 0.0, 0.1, 0.2, 0.3, 0.4, 0.5, 0.6, 0.7, 0.8, 0.9, 1.0

*Typical range of values:* 0 <= Greediness <= 1

Output
-------

**save_shape_matching_model** - saves .shm file with prepared model under *filename* in *file_directory*. Path to file is displayed as *file_toPrint* (or separately *file_toRead* for reading .dxf file and *file_toSave* for saving model in save_shape_matching_model_dxf). The *Output* shows reference image with marked mask (in save_shape_matching_model_mask) or model got from read contours (in save_shape_matching_model_dxf).

**use_shape_matching_model** - marks matching shapes on image with green border and displays their number as *number_of_shapes_found*. Shape with index *ObjectPointer* is marked with purple cross. Parameters of found shapes are returned in arrays such as:

*ShapeCenterX, ShapeCenterY* - coordinates of the center of shape

*ShapeAngle* - rotation of the shape relative to shape model, in radians 

*ShapeScale* - size of the shape relative to shape model. *ShapeScale* > 1 when shape is bigger, *ShapeScale* < 1 when it's smaller

*ShapeScore* - accuracy of matchig, '1' being identical shape

