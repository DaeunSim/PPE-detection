# PPE-Detection
This is a project that uses deep learning to detect PPE for construction workers.

## Dataset (2023-07-03 2:20pm Version)
https://universe.roboflow.com/research-project-i8wzf/ppe-detection-2e7lf/dataset/6 (1,490 images)

## System Environment
* IDE : Kaggle Kernels/Google Colaboratory (NVIDIA Tesla T4 GPUS)
* Language : Python
* Data Labelling Tool : Roboflow (https://roboflow.com/annotate)
* Deep learning model : YOLOv8x

## Implementation
To build a detection model, simply four steps are processed.
* Data collection  
  Ultimately, the YOLO model is used, so the dataset consists of images formatted in YOLO format.
  The dataset includes JPEG images measuring 640 by 640 pixels of personal protective equipment (PPE) worn by people on construction sites, including helmets, high-visibility vests, gloves, and boots.
* Data pre-processing  
  The second step is to capture bounding boxes, which is called labelling.
  Four items were chosen to protect the entire body and were captured (helmet, vest, glove, and boots).
  Afterward, three data agumentation techiniques were applied to increase the dataset's size and
  improve the accuracy of detection results (Flipping, Rotation, and Noise). 3,570 images were used in the end.
* Modeling  
  YOLOv8 (https://github.com/ultralytics/ultralytics) model was used. It is a pre- trained model based on the COCO dataset.
  The COCO dataset consists of 80 different categories of images, and the number of images used to train YOLOv8 is over 140,000 images.
* Evaluation  
  Mean Average Precision (mAP) and F1 score were used as performance indicator.  
  
  
<p align="center">
  <img width="400" height="300" alt="f6" src="https://github.com/DaeunSim/PPE-Detection/assets/49071747/6a30e780-4974-4268-83f9-68ab9bebfffa">
</p>

## Prediction examples
![f9](https://github.com/DaeunSim/PPE-Detection/assets/49071747/3de6153b-c8f9-4cae-a385-1126cec4d635)



