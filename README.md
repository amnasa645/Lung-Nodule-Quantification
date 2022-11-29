# Lung-Nodule-Quantification
Quantify lung nodules on all three axes by using 2D user-defined ROI on a single slice.

## Dataset
[LIDC-IDRI](https://wiki.cancerimagingarchive.net/display/Public/LIDC-IDRI)

## Preprocessing
The preprocessing uses watershed algorithm to segment out the lungs, resizing and resampling of scans.

## Pipeline
In this project, the user provides 2D ROI bounding box of the nodule on one slice. The nodule is then segmented out using 2D Resnet(https://github.com/amalmsaleem/Lung-Nodule-Segmentation). This is shown below:

![image](https://user-images.githubusercontent.com/99807582/199526013-ccc61fdf-6380-4e9f-b38f-c09a1fcb2bcc.png)

The extracted 2D nodule mask is used to generate ROIs in the coronal, sagittal and axial views. Lastly, the ROIs from all the views are combined to give the final mask.

![image](https://user-images.githubusercontent.com/99807582/199523603-dbac19a2-8aaa-44db-85b4-a448269fcaf2.png)
