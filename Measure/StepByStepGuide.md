# Measuring lines/rectangles/circles/ellipse

## One output region

* Use standard function from BVS Cockpit - CheckBlobs - or other function returning region (ex. one these in Blob folder in this repository). Using this function select blobs to be measured.

* Add *measure_lines.hdev* / *measure_rectangle.hdev* / *measure_circles.hdev* / *measure_ellipse.hdev*

* Input regions will be estimated with appropriate shapes and represented by contours. 

*Note: if they're not estimated on default parameters, try decreasing measure_distance or measure_length2 in the first place. Working with measure_line.hdev, try also adjusting values of SelectContours to match range of measured lengths.*  
 
 * Adjust other measurement parameters and chceck if number of measured shapes is as expected.
 
 * Choose one of measured shapes by input *line_to_measure* / *rectangle_to_measure* / *circle_to_measure* / *ellipse_to_measure*.
 
 * Collect output parameters of chosen shape, such as: center coordinates, length etc.

## Multiple output region

* Use standard function from BVS Cockpit - CheckBlobs - or other function returning region (ex. one these in Blob folder in this repository). Using this function select blobs to be measured.

* Add *measure_lines_return_array.hdev* / *measure_rectangle_return_array.hdev* / *measure_circles_return_array.hdev* / *measure_ellipse_return_array.hdev*

* Input regions will be estimated with appropriate shapes and represented by contours. 

*Note: if they're not estimated on default parameters, decrease ArrayCount to be equal or smaller than number of input regions. Also try decreasing measure_distance or measure_length2. Working with measure_line.hdev, try as well adjusting values of SelectContours to match range of measured lengths.*  
 
 * Adjust other measurement parameters and chceck if number of measured shapes is as expected.
 
 * Collect output arrays with parameters of measured shapes.
