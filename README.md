# cv-semantic-segmentation-open3d
We have experimented with many opensource pretrained model for doing semantic segmentation for our paritucular project based on 3D Lidar pointcloud data.
Best working models are
- Myria3D
- cLASpy_T
- Open3dml_RandlaNet_Lilly
- Open3dml_RAndlaNet_Toronto

For Our particular purpose as we needed to segment poles and wires, Open3d_RAndlaNet_Toronto is best fit as it has Pole and Wire classes included.
As this gave the best results among above all the mentioned models.
This model works one 6 features, 3 co-ordinates (X,Y,Z) and 3 Spectral features (Red, Green, Blue).
Basic code is provided by Open3d-ml in their github repo but the key problem was it was working great on their dataset but not on ours.
The solution to this was that we had to do a co-ordinate shift and make it in the same scale as the original test datasets. After that result was bit satisfactory.
