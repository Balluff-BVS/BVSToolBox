# <p align="right"><a class="github-button" aria-label="Download ntkme/github-buttons on GitHub" href="https://github.com/Balluff-BVS/TestScripts/raw/master/DXF/dxf.zip" data-icon="octicon-cloud-download">Download</a></p>

DXF 
=============

## Example

Original Picture             | Extracted Edges
:-------------------------:|:-------------------------:
![Image error](https://github.com/Balluff-BVS/TestScripts/blob/master/DXF/original.png?raw=true)  |  ![Image error](https://github.com/Balluff-BVS/TestScripts/blob/master/DXF/contours_to_save.png?raw=true)

Description
------------

Enables saving and reading .dxf files. 

Writing function gets region as input, generates its contours and saves it in given directory.

Reading function returns contour read from the file as output.

Input parameters
-----------------

**input** - image from which region is extracted (simply obtained by ex. GetImage)

**region_to_save** - region which contours are saved (obtained ex. by CheckBlobs)

**filename** - name of file to be written/read. '.dxf' extention is added automatically while executing a callback. If a file already exists in this directory, it will be overwritten. If this file is open - an exception will be thrown.

**file_directory** - a path to file. As default it is set as /data/icsServer/share/images/, which leads to folder in industrial controller memory. User can customize the path by filling in file_directory field, when working with BVS Cockpit installed on PC.

**mode** - mode of contour generation:

*Default value:* 'border'

*List of values:*

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'border' - The centers of the border pixels are used as contour points.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'center' - The outer border of the border pixels is used as contour points.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;'border_holes' - In addition to the outer border of the input region you get the contours of all holes.

Output
-------------

**dxf_write_callback** generates contours based on input *region_to_save*. After clicking *Excecute* it creates a .dxf file with this contour.

**dxf_read_callback** reads .dxf file, after clicking *Execute*, and loads it to program.

Both functions display *file_toPrint* as an output - whole path to the file in use.
