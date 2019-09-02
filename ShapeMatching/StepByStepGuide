# Creating shape matching models

## Shape matching using mask

* Add *save_shape_matching_model_mask.hdev*

* Capture reference image

* Use wizard to mark shape

* Adjust parameters of model

* Execute *Save* function to save model under the *filename* in *file_directory* 

## Shape matching using region

* Use standard function from BVS Cockpit *CheckBlobs* or other function returning region (ex. one these in *Blob* folder in this repository). Using this function select blob to be saved as shape model

* Add *save_shape_matching_model_region.hdev*

* Choose output region of this function as *model* 

* Adjust parameters of shape model

* Execute *Save* function to save model under the *filename* in *file_directory* 

## Shape matching using .dxf file

* Create .dxf file to be your shape model, ex. using *dxf_write_callback.hdev* from *DXF* folder in this repository.

* Add *save_shape_matching_model_dxf.hdev*

* Execute *Read* function to load .dxf file under the *filename_contours* in *file_directory_contours*. Created shape model will be displayed in *Output*.

* Adjust parameters of shape model

* Execute *Save* function to save shape model under the *filename_model* in *file_directory_model*

# Use saved models

* Add *use_shape_matching_model.hdev*

* Adjust *inputAOI* to cover your region of interest

* Execute *LoadModel* function to load shape model under the *filename_model* in *file_directory_model*

* Adjust shape finding parameters and get results from output arrays
