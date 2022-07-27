# Object detection with MobileNet SSD
Object detection with MobileNet SSD pretrained on the MS COCO dataset and fine-tuned on PASCAL VOC

## Directory Structure

**All the code files and folders follow the following structure.**

```
├── images
│   ├── ima_00.jpg
│   ├── ima_01.jpg
│   ├── ima_02.jpg
│   ├── ima_03.jpg
│   ├── ima_04.jpg
│   ├── ima_05.jpg
│   └── ima_06.jpg
├── outputs
│   ├── output_ima_00.jpg
│   ├── output_ima_01.jpg
│   ├── output_ima_02.jpg
│   ├── output_ima_03.jpg
│   ├── output_ima_04.jpg
│   ├── output_ima_05.jpg
│   └── output_ima_06.jpg
├── MobileNetSSD_deploy.caffemodel
├── MobileNetSSD_deploy.prototxt.txt
├── README.md
├── object_detection.py
└── requirements.txt

```


## Introduction

It is used MobileNet SSD (Single Shot Detector), which has been trained on the MS COCO dataset and was then fine-tuned on PASCAL VOC reaching 72.7% mAP.  SSD models are generally faster when compared to other object detection models. Moreover, the MobileNet backbone also makes them less compute-intensive.

We can therefore detect 20 objects in images (+1 for the background class), including airplanes, bicycles, birds, boats, bottles, buses, cars, cats, chairs, cows, dining tables, dogs, horses, motorbikes, people, potted plants, sheep, sofas, trains, and tv monitors.



## Instructions

Please, make sure you have all the requirements installed. Please read the rquirements.txt located in the main folder

To run the code in Python, please go into the main folder and execute the Python scripts detect_img.py adding the image route argument, the prototxt route argument and the model route argument. Example:

```
py object_detection.py --image images/ima_01.jpg --prototxt MobileNetSSD_deploy.prototxt.txt --model MobileNetSSD_deploy.caffemodel
```


## Outputs

Object detection images are saved in:
```
 outputs/object_detections_image.jpg
 ```
