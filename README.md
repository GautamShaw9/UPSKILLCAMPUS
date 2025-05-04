# Crop and Weed Detection using YOLOv5

This project uses the YOLOv5 object detection algorithm to identify and classify crops and weeds in agricultural field images.

## Project Overview

- *Goal*: Detect and classify crops and weeds using a custom-trained YOLOv5 model.
- *Model*: YOLOv5s (small version for faster training and inference)
- *Dataset*: Custom-labeled images (split into train and val folders)
- *Result*: Trained weights (best.pt) for use in real-time or batch detection.

## Folder Structure

Crop-Weed-Detection/
├── agri_dataset/ │ 
├── images/   
│   ├── train/   
│   └── val/   
├── labels/ │   
│   ├── train/ 
│   └── val/ 
├── yolov5/ 
│    ├── best.pt ├── detect.py ├── train.py 
└── README.md

## Steps to Run

### 1. Clone YOLOv5

git clone https://github.com/ultralytics/yolov5
cd yolov5
pip install -r requirements.txt

2. Train the Model

python train.py --img 640 --batch 16 --epochs 20 --data ../agri_dataset.yaml --weights yolov5s.pt --name crop-weed

3. Run Detection

python detect.py --weights runs/train/crop-weed/weights/best.pt --img 640 --source ../agri_dataset/images/val

Results

Model successfully trained to detect and differentiate between crops and weeds.

Trained weights are saved as best.pt.


Contributor
Gautam Shaw
