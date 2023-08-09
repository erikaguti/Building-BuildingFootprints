# Building Building Footprints

This notebook trains a U-Net convolutional neural network to extract building footprints from aerial images taken in Massachusetts. 

The image data consists of 3347 colour raster of dimension 256x256x3 using the NAD83 (EPSG:26986) projection system. Each raster represents an area of 300 square meters. The label data consists of building footprints vectors extracted from [OpenStreetMap](https://www.openstreetmap.org/relation/61315) and converted into a binary raster with the same extent and resolution as the image rasters. The unformatted data was provided by Minh (2013) and can be accessed on his [website](http://www.cs.toronto.edu/~vmnih/data/). Images and labels are randomly partitioned into a training (70%) validation (15%) and test sample (15%).

The U-Net convolutional neural network is coded in Tensorflow. Adam is used as an optimizer and Binary Focal Cross Entropy as the loss function. In Step 8 a spatial dropout layer is applied to enhance performance. The model was trained for 30 epochs with a batch size of 32. It had a loss of .04 and an accuracy of .9


Diagram of the U-Net convolutional network:
![model 2](https://github.com/erikaguti/Building-BuildingFootprints/assets/57955273/e8b8532f-d764-4b63-bb1f-b366c186ff8f)

Example of model output:
<img width="1201" alt="Screenshot 2023-08-09 at 5 57 57 PM" src="https://github.com/erikaguti/Building-BuildingFootprints/assets/57955273/69177f23-06d6-4b7c-bcf4-bd16f3b91f11">






