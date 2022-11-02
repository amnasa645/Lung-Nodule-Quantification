# Lung-Nodule-Quantification

Cancer is one of the leading causes of death around the world. Early detection is a crucial step to surviving. Commonly, radiologists detect nodules using MIPs of different thicknesses. Maximum Intensity Projections (MIP) help visualize lung features over multiple scans, hence giving a clearer picture of nodules and vessels, as nodules are isolated specs and vessels, like veins, are continuous. This is better demonstrated in the figure below:

![output](https://github.com/amalmsaleem/Lung-Nodule-Segmentation/blob/main/Images/image1.png)

## Preprocessing
The preprocessing uses watershed algorithm to segment out the lungs, resizing and resampling of scans.

## Pipeline
In this project, the user provides 2D ROI bounding box of the nodule on one slice. The nodule is then segmented out using the results of my project [here](https://github.com/amalmsaleem/Lung-Nodule-Segmentation). This is shown below:

![image](https://user-images.githubusercontent.com/99807582/199526013-ccc61fdf-6380-4e9f-b38f-c09a1fcb2bcc.png)

The extracted 2D nodule mask is used to generate ROIs in the coronal, sagittal and axial views. Lastly, the ROIs from all the views are combined to give the final mask.

![image](https://user-images.githubusercontent.com/99807582/199523603-dbac19a2-8aaa-44db-85b4-a448269fcaf2.png)
