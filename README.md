# Pothole-Detection-YoloV5

## Dataset URL
https://www.kaggle.com/datasets/chitholian/annotated-potholes-dataset?select=annotated-images

## Problem Statement

Object Detection on the potholes present on the roads with YoloV5

## About Data
This dataset contains 665 annotated images of potholes.
Bounding box annotations are provided in the PASCAL VOC format.

## Analysis
1. The analysis has been done on `Google Colab Environment`
    - Model training has been done on the notebook `YoloV5_Pothole_Model_Training.ipynb`
    - Model inferencing has been done on the notebook `YoloV5_Pothole_Pretrained_Model_Inferencing.ipynb`
    - Model inferencing with OpenCV DNN Module has been done on the notebook `YoloV5_Inferencing_With_OpenCV_DNN.ipynb`


2. Convert the PASCAL VOC `.xml` format to Yolo `.txt` format


3. Train Test Split
    - Number of train images: 532
    - Number of test images: 133
    
    
4. Setup for YoloV5
    - Clone the YoloV5 git repository: https://github.com/ultralytics/yolov5
    - Install YoloV5
    
    
5. Create custom `pothole_detection.yaml` for model training


6. Train the Model
    - Pretrained Weights: `yolov5x.pt`
    - Epochs: 100
    - Batch Size: 16
    - Image Size: 416X416
    
    
7. Evaluation
    - mAP@.5 ---> 0.81
    - mAP@.5:.95 ---> 0.533
    
    
8. Convert the `best.pt` model weights to `best.onnx` for further inferencing with OpenCV DNN


9. Model Inferencing with OpenCV DNN Module
    - No need to setup YoloV5
    - Just need the latest version of `opencv-python` library for inferencing the YoloV5 model
    - Use the `best.onnx` model weights

## Result:

![alt text](https://github.com/Suvam-Bit/Pothole-Detection-YoloV5/blob/main/sample_video_outputs/output.gif?raw=true)
