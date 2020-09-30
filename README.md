# Ship-Detection-from-Satellite-Images

### Introduction
Shipping traffic is growing fast. More ships increase the chances of infractions at sea like environmentally devastating ship accidents, piracy, illegal fishing, drug trafficking, and illegal cargo movement. This has compelled many organizations, from environmental protection agencies to insurance companies and national government authorities, to have a closer watch over the open seas.

In this project, we need to locate ships in the satellite images by putting an aligned bounding box segment around the ships. Given the input image (satellite image), the model gives an output of the same image with bounding boxes on the ships wherever they are located. Also, our next main goal is to identify the ship in the image as quickly and as accurately as possible.
In this scenario, many images may not contain ships, and those that do, may contain multiple ships. Ships within and across images may differ in size (sometimes significantly) and be located in open sea, at docks, marinas, etc. And moreover, the satellite images obtained, may have the images with clouds or haze. So, we have to overcome all these challenges and locate the ships in the satellite image.

### Data
In the dataset, we have satellite images which consist of images containing ships and the images which don’t have ships. However, both classes are equally distributed. We are acquiring our dataset from Kaggle.
In the images containing the ships, we have a slight overlap of object segments when ships were directly next to each other. Ships within and across images may differ in size (sometimes significantly) and be located in open sea, at docks, marinas, etc. And moreover, the satellite images obtained, also have the images with clouds or haze. 
So, to overcome them, any segments overlaps were removed by setting them to background (i.e., non-ship) encoding. Therefore, some images have a ground truth may be an aligned bounding box with some pixels removed from an edge of the segment. These small adjustments will have a minimal impact on accuracy.
Also, the dataset present here is a huge dataset, so we need to handle it by taking fractions of data and building our model.
Web link to the dataset: https://www.kaggle.com/c/airbus-ship-detection/data

