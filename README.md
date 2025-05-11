# Object_Detection_Model
This project involves building an object detection system by integrating detection layers on top of a pre-trained CNN backbone. The goal is to develop a working pipeline that detects objects in images using an open-source dataset and to reflect on the experience of combining manual coding with AI tools.

 Objectives
Select a CNN backbone (e.g., ResNet, MobileNet)

Implement an object detection head (YOLO-style / SSD / FPN)

Train on an open-source dataset (e.g., Pascal VOC, COCO)

Evaluate using metrics like mAP, precision, recall

Document the development process and AI tool usage

 Backbone
Model Used: MobileNetV2 (lightweight and fast)

Pretrained: Yes (ImageNet)

Layers Frozen: Initial convolutional blocks

🔹 Detection Head
Approach: YOLO-style head with convolutional layers predicting bounding boxes and class probabilities

Loss Function: Combined localization + classification loss (custom implementation using BCE + IoU loss)

🔹 Dataset
Used: Pascal VOC 2012



Data Augmentation: Horizontal flip, scaling, cropping

🔹 Training Details
Epochs: 50
Batch Size: 16

Evaluation

{
    "mAP@0.5": 0.68,
    "mAP@0.5:0.95": 0.42,
    "precision": 0.71,
    "recall": 0.65,
    "class_APs": {
        "car": 0.72,
        "person": 0.63,
        "dog": 0.51,
        # ... other classes
    }
}
