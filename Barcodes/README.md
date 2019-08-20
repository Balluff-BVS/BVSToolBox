# <p align="right"><a class="github-button" aria-label="Download ntkme/github-buttons on GitHub" href="https://github.com/Balluff-BVS/TestScripts/raw/master/Barcodes/read_barcode.zip" data-icon="octicon-cloud-download">Download</a></p>

READ BARCODE
===========
Example
---------
<p align="center">
  <img src="https://github.com/Balluff-BVS/TestScripts/blob/master/Barcodes/barcodes_img.PNG?raw=true" alt="Picture error">
</p>

Description
----------
Detects and reads bar code symbols in an image.

Enables setting up to 18 parameters to improve detection. User may choose one of read codes and check its correctness. Red pointer marks the code which value is currently displayed. 

Input parameters
--------------
**check_char** - When set to 'present', a check character is expected and used to verify the 
		correctness of the bar code. No bar code result is returned if the check 
		sum does not match, and the check character itself is stripped from the 
		data. If this stripping is undesired, the mode 'preserved' allows to verify
		the bar code while still keeping the check character in the data.
    
*Default:* 'absent'
    
*List of values:* ['absent', 'present', 'preserved']

**composite_code** - If 'composite_code' is set to 'CC-A/B' the composite component will be found and decoded.

*Default:* 'none'

*List of values:* ['none', 'CC-A/B']

**barcode_height_min** - Minimal bar code height. The value of this parameter is defined in pixels.

*Default:* -1

*Suggested values:* [-1, 8 ... 64]

**barcode_width_min** - Minimal bar code width.

*Default:* -1

*Suggested values:* [-1, 40, 50, 60, ...]

**element_size_max** - Maximal size of the base bar code elements (also called 'modules' 
			or 'narrow bars', depending on the specific bar code type)
      
*Default:* 8.0

*Suggested values:* [4.0 ... 60.0]
			
**element_size_min** - Minimal size of the base bar code elements (also called 'modules' 

*Default:* 2.0

*Suggested values:* [1.2 ... 10.0]

**contrast_min** - Minimal contrast between the foreground and the background of the bar code elements.

*Default:* 0

*Suggested values:* [0, 40, 90, 120, ... ]

**meas_thresh** - Defines a threshold which is a relative value with respect to the dynamic 
		range of the scanline pixels.

*Default:* 0.05

*Suggested values:* [0.05 ... 0.2]

**meas_thresh_abs** - If the threshold value based on 'meas_thresh' gets smaller than the 
			value of 'meas_thresh_abs', the latter is used as threshold instead.
      
*Default:* 5.0

*Suggested values:* [0.0 ... 10.0]

**min_identical_scanlines** - The parameter specifies the minimal number of decoded scanlines
			which return identical data to read the bar code successfully.
      
*Default:*

| Barcode Type    | min_identical_scanlines |   
|-----------------|-------------------------|
| 2/5 Industrial  | 2                       |
| 2/5 Interleaved | 2                       |
| all others      | 0                       |

        
*Suggested values:* [0, 2, 3, ...]

			
**majority_voting** - If this parameter is 'false', a successful decode result is returned 
			if the minimal number of identically decoded scanlines are found 
			(see section on 'min_identical_scanlines' for more details). 
			By setting this parameter to 'true' a majority voting scheme is 
			used to select between different scanline results.
      
*Default:* 'false'

*List of values:* ['false', 'true']

**num_scanlines** - Maximum number of scanlines used during the scanning of 
			a (candidate) bar code.
      
*Default:* 0

*Suggested values:* 0, 5, 10, 20 ...

**orientation** - Expected bar code orientation.

*Default:* 0.0

*Suggested values:* [-90.0 ... 90.0]

**start_stop_tolerance** - Enforces a tolerant ('high') or strict ('low') searching criteria 
			while inspecting a scanline for a start or stop pattern
      
*Default:* 'high'

*List of values:* ['high', 'low']	

**stop_after_result_num** - Number of successfully decoded bar codes after which 
				the decoding will stop.

*Default:* 0

*Suggested values:* [0, 1, 2, ...]

**upce_encodation** - By default, 'upce_encodation' is set to 'ucc-12' and the decoded 
			string will be returned in UCC-12 format (consisting of 12 digits).
			If 'upce_encodation' is set to 'zero-suppressed', the result will 
			be returned in zero-suppressed format 
			(with suppressed zeros at defined places).
      
*Default:* 'ucc-12'

*List of values:* ['ucc-12', 'zero-suppressed']

**min_code_length** - Minimal number of decoded characters.

*Default:*

| Barcode Type    | min_code_length |
|-----------------|-----------------|
| 2/5 Industrial  | 3               |
| 2/5 Interleaved | 3               |
| all others      | 0               |

*Suggested values:* [0, 1, 2, ...]

**merge_scanlines** - If not enough scanlines (see 'min_identical_scanlines') can be read 
			successfully, i.e., because the bar code is partly occluded or 
			damaged, an attempt is being made to merge the existing scanlines. 
			Then, these merged scanlines are decoded again.

*Default:* 'true'

*List of values:* ['true', 'false']

**code_to_print** - index of code to print

**code_to_check** - value of code to compare with code 

Output
---------
Regions containing detected barcodes.

**number_of_codes_found** - how many barcodes are detected on the image

**decoded_data** - string with code read from region marked with red pointer.

**correctness** - information whether *decoded_data* is the same as *code_to_check*

Additionally, all input parameters are displayed as output.
