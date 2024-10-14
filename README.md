# Tumor Cell Classification in Histopathological Images Using Deep Learning

## Project Overview

This repository contains a deep learning model designed for the classification of malignant tumors in breast histopathology images. The primary focus of this project is to assist medical professionals in diagnosing breast cancer by leveraging computer-aided diagnosis (CAD) through the YOLOv5 model. The aim is to support accurate and efficient medical diagnosis by utilizing state-of-the-art computer vision techniques to detect malignant tumors in histopathological images.

## Key Features

- **Model:** YOLOv5 (You Only Look Once), a real-time object detection model.
- **Objective:** Classify and detect malignant tumor cells in histopathological images.
- **Dataset:** Breast cancer histopathology images from the TCGA dataset, containing images of 1,098 patients.
- **Performance:** Achieved an accuracy of 81% in tumor classification.
- **Tools Used:** Python, LabelImg, Label Studio for image annotation, YOLOv5 for detection, and standard deep learning libraries such as PyTorch.

## Dataset

The dataset used for this project includes histopathological images from the TCGA-BRCA database. Images were manually annotated by a specialist using LabelImg and Label Studio tools. Tumor regions were labeled to provide the ground truth for training the YOLOv5 model. 

You can access the dataset [here](https://portal.gdc.cancer.gov/projects/TCGA-BRCA).

## Model Training and Validation

- **Preprocessing:** Images were divided into training and validation sets, with 57 images used for training and 14 images for validation.
- **Annotation:** A total of 1,224 objects (tumors) were annotated across the dataset.
- **Training:** The model was trained for 250 epochs with a batch size of 16, using a pre-trained YOLOv5s model for transfer learning.
- **Metrics:** Precision, recall, F1-score, and mean average precision (mAP) were calculated to evaluate the performance.

## Results

- **Accuracy:** 81%
- **mAP@0.5:** 0.74
- **mAP@0.5:0.95:** 0.383

The model was able to detect tumors with high precision, especially at confidence thresholds below 0.8. It was noted that the model's performance is promising for use as a diagnostic aid, though it does not replace a pathologist's diagnosis.

## References

- [YOLOv5 Documentation](https://github.com/ultralytics/yolov5)
- [TCGA-BRCA Dataset](https://portal.gdc.cancer.gov/projects/TCGA-BRCA)
