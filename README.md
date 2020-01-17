# map_validation
Codes for validation of land use maps

In the first step a stratified random sample is taken from the land use map to create a set of reference points. This set of points will be used by the evaluator(s) to identify the land use or land use changes from orthophotos. During the second step, the set of reference points is used to construct a confusion matrix and calculate the accuracy and estimates of the map classes.

Prior to the sampling step, the map is preprocessed in ArcGIS. The entire raster map with the change classes (e.g. between 2013 and 2016) is converted to a vector point layer, xy-coordinates are added and the points are exported as a .csv table. For the validation of the land use classes (area), the number of points would be too large when vectorising the entire LU map. Therefore, a . This subset of vectorised raster cells is then exported as a .csv table.

## Step 1 - Code for stratified random sampling of LU points

With the first code (StratifiedRandomSample_Area/Change) a stratified random sample is taken from the land use map. This map can be a change layer (changes between 2 periods) or a state layer (area of each LU class). The first layer is used for the validation of land use changes, the second for the validation of the area estimates of each land use class.

The exported reference points are used as input, together with a table holding the codes of the land use classes, the area of each LU class and the estimated user's accuracies of each class. 

## Step 2 - Code for validation of LU maps

The second code (Validation_Area/Change) is used for the calculation of map accuracies and area estimates.
