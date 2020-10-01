Ship detection from remote sensing imagery is a crucial application for maritime security which includes among others traffic surveillance, protection against illegal fisheries, oil discharge control and sea pollution monitoring. This is typically done through the use of an Automated Identification System (AIS), which uses VHF radio frequencies to wirelessly broadcast the ships location, destination and identity to nearby receiver devices on other ships and land-based systems.
AIS are very effective at monitoring ships which are legally required to install a VHF transponder, but fail to detect those which are not, and those which disconnect their transponder. So how do you detect these uncooperative ships? This is where satellite imagery can help. Synthetic Aperture Radar (SAR) imagery uses radio waves to image the Earth’s surface. Unlike optical imagery, the wavelengths which the instruments use are not affected by the time of day or meteorological conditions, enabling imagery to be obtained day or night, with cloudy, or clear skies. Satellites are collecting these images which could be used to make algorithms for ship detection and segmentation.

This project is a part of the Airbus Ship Detection Challenge held on Kaggle.

### Data
In the dataset, we have satellite images which consist of images containing ships and the images which don’t have ships. However, both classes are equally distributed. We are acquiring our dataset from Kaggle.
In the images containing the ships, we have a slight overlap of object segments when ships were directly next to each other. Ships within and across images may differ in size (sometimes significantly) and be located in open sea, at docks, marinas, etc. And moreover, the satellite images obtained, also have the images with clouds or haze. 
So, to overcome them, any segments overlaps were removed by setting them to background (i.e., non-ship) encoding. Therefore, some images have a ground truth may be an aligned bounding box with some pixels removed from an edge of the segment. These small adjustments will have a minimal impact on accuracy.
Also, the dataset present here is a huge dataset, so we need to handle it by taking fractions of data and building our model.


Web link to the dataset: https://www.kaggle.com/c/airbus-ship-detection/data



![alt text](https://miro.medium.com/max/875/1*LIXHle36qz-ueqtC5wo0lA.png)
